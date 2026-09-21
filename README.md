# cochin.fr

Source of [www.cochin.fr](https://www.cochin.fr), Philippe Cochin's personal site. It is a [Jekyll](https://jekyllrb.com/) site served by GitHub Pages, using the [minima](https://github.com/jekyll/minima) theme in its dark skin.

## Layout

- `index.md` - home page; the theme lists the posts below its text
- `ai.md`, `quantum.md`, `math.md`, `certifications.md`, `about.md` - the header pages, in the order given by `minima.nav_pages` in `_config.yml`
- `_posts/` - blog posts (conference notes, in English or French); the file name sets the URL, the front matter sets the date
- `assets/images/` - images
- `CNAME` - the custom domain

## Building

GitHub Pages builds the `master` branch with its legacy builder on every push. There is no CI workflow and no lock file: the builder uses its own pinned gem set from the `github-pages` gem and never reads `Gemfile.lock`, so the lock is ignored on purpose (see `.gitignore`).

To preview locally without installing Ruby, run from the repository root:

```bash
docker run --rm -it -p 4000:4000 -v "$PWD:/site" -w /site ruby:3.3 bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

and open <http://localhost:4000>.

## Theme

`remote_theme` in `_config.yml` pins minima to a specific upstream commit, so an upstream change cannot alter the live site unannounced. To pick up newer theme changes, replace the commit hash with a recent one from <https://github.com/jekyll/minima/commits/master>, push, and check the site still renders.
