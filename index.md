---
layout: default
---
# About Me 
```yaml
apiVersion: bienkma.github.io/v1
kind: person
spec:
  name: bien
  age: "> 25"
  gender: man
  languages: # in order of proficiency
    - Vietnamese
    - English
  education:
    - Academy of Cryptography Techniques (2015-2017) # The Master of Information security 
    - Academy of Cryptography Techniques (2005-2010) # Information security engineer
    - Won first prize in Student Contest on Information Security 2010 - Vietnam
    - LPI-1
    - CKA
    - PCIDSS
  code: # in order of proficiency
    - bash
    - golang
    - python
  infrastructure: # in order of proficiency
    general:
    - Solid understanding of linux, virtualization/container and performance, security, and scalability.
    automation: # have been operating and managing for more than 3 years
      - ansible
      - terraform
    devops: # have been operating and managing for more than 3 years
      - k8s
      - docker
      - jenkins, argocd
    bigdata: # I built 10PGB and 8PGB big data clusters based on Hortonworks and Cloudera platform at on-premise
      - hadoop
      - kafka
      - zookeeper
      - spark
      - Sqoop
      - Hbase
      - hive
      - pig
    database: # have been operating and managing for more than 3 years
      - MySQL (percona distribute)
      - Redis
      - Mongodb
      - Postgresql
    webserver: # have been operating and managing for more than 3 years
      - nginx
      - apache
    loadbalancing: # have been operating and managing for more than 3 years
      - LVS/Keepalived (DR, NAT, Tunnel model)
      - Haproxy
      - Katran
      - BGP
    monitoring: # have been operating and managing for more than 3 years
      - ELK stack
      - Prometheus/VictoriaMetrics
      - Telegraf
      - Nagios/cacti (NRPE, SNMP)
```
# My Notes 
- [Principle](#principle)
- [Coding](#coding)
- [Networking](#networking)
- [Infrastructure](#infrastructure)
- [Security](#security)
- [Organization](#organization)
- [Talk](#talk)

## Principle
* [NoSQL vs. SQL: Important Differences & Which One Is Best for Your Project](https://www.upwork.com/resources/nosql-vs-sql)
* [System Design - bytebytego](https://bienkma.github.io/books/system-design-arch.pdf)
* [Design Patterns](https://refactoring.guru/design-patterns)

## Coding
* [Mastering WebSockets With Go](https://programmingpercy.tech/blog/mastering-websockets-with-go/)
* [Multiplexing Explained - Redis](https://redis.com/blog/multiplexing-explained/)

## Networking
* [Demystifying DCN Topologies: Clos/Fat Trees – Part1](https://packetpushers.net/blog/demystifying-dcn-topologies-clos-fat-trees-part1/)
* [Demystifying DCN Topologies: Clos/Fat Trees – Part2](https://packetpushers.net/blog/demystifying-dcn-topologies-clos-fat-trees-part2/)
* [What Is a Microburst? How to Detect a Microburst?](https://support.huawei.com/enterprise/en/doc/EDOC1100086962)
* [Cloud - Multi region - DCI - arista](https://bienkma.github.io/books/DCI-400G.pdf)
* [APAC Cloud Builders 2023](https://github.com/bienkma/bienkma.github.io/blob/master/books/APAC-Cloud.pdf)
* [how-to-build-a-nxos-9000v-based-evpn-vxlan-fabric](https://www.packetcoders.io/how-to-build-a-nxos-9000v-based-evpn-vxlan-fabric/#limitations3.1.2)
* [VXLan & GRE in Vietnamese Langguage](https://github.com/hocchudong/thuctap012017/blob/master/XuanSon/Netowork%20Protocol/VXLAN-GRE%20Protocol.md)
* [Overlay Tunneling with Open vSwitch - GRETAP, VXLAN, Geneve, GREoIPsec](https://costiser.ro/2016/07/07/overlay-tunneling-with-openvswitch-gre-vxlan-geneve-greoipsec/#.V8RUmx-g9Xh)
* [VXLAN Series](https://blogs.vmware.com/vsphere/2013/04/vxlan-series-different-components-part-1.html)
* [KVM Overlay Network with VXLAN](https://blog.dama.lol/kvm-overlay-network-with-vxlan)
* [VXLAN: BGP EVPN with FRR](https://vincent.bernat.ch/en/blog/2017-vxlan-bgp-evpn)
* [Open Virtual Network (OVN)](https://docs.ovn.org/_/downloads/en/stable/pdf/)

## Infrastructure
* [How to setup data at rest encryption on Ubuntu](mysharing/database/data-at-rest.md)
* [Howto setup many services on Centos](https://www.server-world.info/en/note)
* [OVN SSL setup for Openstack](https://satishdotpatel.github.io/ovn-ssl-setup-with-openstack)
* [Optimizing Computer Applications for Latency: Part 1: Configuring the Hardware](https://www.intel.com/content/www/us/en/developer/articles/technical/optimizing-computer-applications-for-latency-part-1-configuring-the-hardware.html)
* [Performance Tuning with tuned and tuned-adm](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/7/html/performance_tuning_guide/sect-red_hat_enterprise_linux-performance_tuning_guide-performance_monitoring_tools-tuned_and_tuned_adm#sect-Red_Hat_Enterprise_Linux-Performance_Tuning_Guide-Performance_Monitoring_Tools-tuned_and_tuned_adm)

## Architecture
* [ByteByteGoHQ System Design 101](https://github.com/ByteByteGoHq/system-design-101)

## Security
* [Bamboo Firewall ](https://github.com/bamboo-firewall)

## Organization
* [ByteDance Open Sources Its Cloud Native Data Warehouse ByConity](https://byconity.github.io/blog/2023-05-24-byconity-announcement-opensources-its-cloudnative-data-warehouse)
* [Log analytics using ClickHouse](https://blog.cloudflare.com/log-analytics-using-clickhouse/)
* [SigNoz - Logs Performance Benchmark](https://signoz.io/blog/logs-performance-benchmark/?utm_source=github&utm_medium=logs-benchmark)

## Talk
* [Policy as code with bamboo firewall](https://github.com/bamboo-firewall/docs/blob/main/case-studies/PaC-with-bamboofw.pdf)
