# frozen_string_literal: true

source "https://rubygems.org"

# Ruby 3.4+ no longer bundles these stdlibs by default; Jekyll and deps still require them.
gem "base64"
gem "bigdecimal"
gem "csv"
gem "logger"
gem "ostruct"

# Transitive via html-proofer / w3c_validators; pin so GitHub Security / libxml2 CVEs stay patched.
gem "nokogiri", ">= 1.18.9"

gemspec
