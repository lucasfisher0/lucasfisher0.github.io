# frozen_string_literal: true

source "https://rubygems.org"

gem 'jekyll', '~> 4.4.1' # comment out for GH pages
gem 'jekyll-sass-converter', '~> 3.1' # requires remote-theme patch below
# gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins # Find version at: https://pages.github.com/versions/
gem "minima", github: "jekyll/minima", ref: "ded17a1"

group :jekyll_plugins do
  gem 'jekyll-feed', '~> 0.17.0'
  #gem 'jekyll-remote-theme', '~> 0.4.3'
  gem 'jekyll-seo-tag', '~> 2.8'
  gem 'jekyll-toc'

  # Patched jekyll-remote-theme to allow for newest SASS converter
  # https://github.com/benbalter/jekyll-remote-theme/pull/103/commits/ccd10b4fa18479df5cb508707b269a43a935cd09
  gem "jekyll-remote-theme", github: "benbalter/jekyll-remote-theme", ref: "ccd10b4"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
# gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]
gem 'wdm', '~> 0.2.0' if Gem.win_platform?

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
