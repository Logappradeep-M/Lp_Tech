# frozen_string_literal: true

source "https://rubygems.org"
gem "jekyll"
gemspec

group :test do
  gem "html-proofer", "~> 5.0"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.8.0", :platforms => [:jruby]

# Lock jekyll-sass-converter to 2.x on Linux-musl
if RUBY_PLATFORM =~ /linux-musl/
  gem "jekyll-sass-converter", "~> 3.0"
end
gem "nokogiri", "~> 1.16.0"
gem "parallel", "~> 1.24.0"
gem "rainbow", "~> 3.1.1"
gem "typhoeus", "~> 1.4.1"
gem "yell", "~> 2.2.2"
gem "zeitwerk", "~> 2.6.12"
gem "racc", "~> 1.7.3"
gem "ethon", "~> 0.16.0"
