# Only needed if you want to preview the site on your own computer.
# GitHub Pages builds the live site itself; you do not need Ruby to publish.
source "https://rubygems.org"
gem "github-pages", ">= 232", group: :jekyll_plugins
gem "webrick"   # needed for `jekyll serve` on Ruby 3+
# No longer bundled with Ruby 3.4+ but still required by GitHub Pages' Jekyll
gem "csv"
gem "base64"
gem "bigdecimal"
gem "logger"
gem "ostruct"
platforms :windows do
  gem "tzinfo-data"
  gem "wdm", ">= 0.1.0"
end
