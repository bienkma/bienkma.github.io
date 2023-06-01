# Giới thiệu
- Một trong các yêu cầu đảm bảo thông tin là dữ liệu lưu trữ phải được mã hoá, bảo vệ để chống khả năng hacker tái sử dụng được các phần dữ liệu lưu trữ phía dưới để đánh cắp dữ liệu. LUKS - Linux Unified Key Setup được Redhat phát triển là 1 trong các giải pháp sẽ giải quyết vấn đề mã hoá dữ liệu mức block. 
- Ưu điểm của giải pháp là trong suốt với lớp dịch vụ, ứng dụng phía trên nghĩa là nó tương thích hoàn toán với các dịch vụ phía trên. Chính vì thế để đảm bảo tính năng Data at rest encryption cho MySQL, Elasticsearch, Mongodb... hoàn toàn độc lập với solution sẽ sử dụng. Ngoài ra việc vận hành, cài đặt LUKS device là tương đối đơn giản và đặc biệt hiệu năng của LUKS và device ban đầu không bị ảnh hưởng nhiều (tôi đã thử benchmark với percona 5.7 dung lượng db 20TB/40TB SSD - raid0, 256GB RAM, 112 CPU - tốc độ đọc ghi trước và sau khi enable LUKS tăng chỉ 2-5% resource CPU và IOPS).
- Nhược điểm: Mã hoá mức block nên việc 1 hacker truy cập được mức OS hoặc dịch vụ vẫn có thể lấy được data trước mã hoá của dịch vụ, db. Tóm lại, chỉ chống được physical attack không giải quyết được logical attack.
# Cấu hình
- Cấu hình lab:
  - Ổ cứng cần mã hoá đặt tại /dev/sdb 
  - Hệ điều hành: Ubuntu 22.04
- Các câu lệnh thực hiện mã hoá:
```sh
wipefs --all --backup /dev/sda
lsblk
pvcreate /dev/sda
vgcreate data /dev/sda
lvcreate -l +100%free -n data01 data
cryptsetup --verbose --verify-passphrase luksFormat  /dev/data/data01
cryptsetup luksOpen /dev/data/data01 data
mkdir -p /data
mkfs.xfs -f /dev/mapper/data
```
  - Lệnh này chỉ chạy khi ổ cứng sdb của bạn là SSD hoặc NVMe thôi nhé. Mục đích là không cần cơ chế quản lý queue của OS [here](https://www.cloudbees.com/blog/linux-io-scheduler-tuning)
```sh
echo none > /sys/block/sdb/queue/scheduler
```
  - Add vào crypttab để nó tự boot khi server khởi động lại
```sh
vi /etc/crypttab
mkdir -p /etc/data-at-rest/
cat /etc/crypttab
vi /etc/data-at-rest/data-data01
chmod 400 etc/data-at-rest/data-data01
chmod 0400 /etc/data-at-rest/data-data01
chmod 0744 /etc/data-at-rest
cryptsetup -v luksAddKey /dev/data/data01 /etc/data-at-rest/data-data01
```