source "https://rubygems.org"

# GitHub Pages builds the site with its own pinned gem set and never reads this
# file; it only serves the local preview described in README.md. The
# github-pages gem brings the same Jekyll and the same plugins as production,
# including jekyll-remote-theme, which fetches the minima commit pinned in
# _config.yml.
gem "github-pages", group: :jekyll_plugins

# Ruby 3 no longer ships webrick, which `jekyll serve` needs.
gem "webrick", "~> 1.8"

# Windows and JRuby do not include zoneinfo files.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
