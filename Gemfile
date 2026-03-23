
source "https://rubygems.org"

# Use GitHub Pages's dependency versions
gem "github-pages", group: :jekyll_plugins

# Optional: Add extra plugins here
# group :jekyll_plugins do
#   gem "jekyll-feed"
# end

# Compatibility gems for Windows/JRuby
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# Required for Ruby 3+
platforms :ruby_30 do
  gem "webrick", "~> 1.8"
end
