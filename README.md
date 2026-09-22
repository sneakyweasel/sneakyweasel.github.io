# cochin.fr

Source of [www.cochin.fr](https://www.cochin.fr), Philippe Cochin's personal site. It is a [Jekyll](https://jekyllrb.com/) site served by GitHub Pages, using the [minima](https://github.com/jekyll/minima) theme in its auto skin (light or dark from the visitor's system setting), in English and in French.

## Layout

- `index.md` - English home page; the layout lists the English posts below its text
- `ai.md`, `quantum.md`, `math.md`, `code.md`, `art.md`, `certifications.md`, `about.md` - the English header pages, in the order given by `minima.nav_pages` in `_config.yml`
- `fr/` - the French pages, same file names, served under `/fr/` with the same slugs; the French header order is `minima.nav_pages_fr`
- `_posts/` - English blog posts; the file name sets the URL, the front matter sets the date
- `_billets/` - French blog posts, a collection served under `/fr/`; each carries its `date` and `permalink` in its front matter
- `_includes/` and `_layouts/` - copies of the theme's head, header, footer, home and post files adapted for two languages, plus `i18n.html` (the language variables) and `date.html` (a date in the page's language)
- `assets/images/`, `assets/certificates/`, `assets/icons/` - images
- `CNAME` - the custom domain

## Two languages

Every page and post has a `ref` in its front matter shared with its translation (`ref: math` on `math.md` and `fr/math.md`). `_includes/i18n.html` reads it to find the page's counterpart, which the header toggle links to and the `hreflang` links in the head point at; a page without a translation toggles to the other language's home page. The `lang` of a document comes from its directory through `defaults` in `_config.yml`, so a new file needs no `lang` line.

To add a page: write it at the root and in `fr/` with the same `ref`, and list both in `nav_pages` and `nav_pages_fr`. To add a post: write `_posts/YYYY-MM-DD-slug.md` and `_billets/YYYY-MM-DD-slug.md` with the same `ref`; the French one also needs `date` and `permalink` (`/fr/ai/YYYY/MM/DD/slug.html`). The English feed is `/feed.xml`, the French one `/fr/feed.xml`.

## Building

GitHub Pages builds the `master` branch with its legacy builder on every push. There is no CI workflow and no lock file: the builder uses its own pinned gem set from the `github-pages` gem and never reads `Gemfile.lock`, so the lock is ignored on purpose (see `.gitignore`).

To preview locally without installing Ruby, run from the repository root:

```bash
docker run --rm -it -p 4000:4000 -v "$PWD:/site" -w /site ruby:3.3 bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

and open <http://localhost:4000>.

## Theme

`remote_theme` in `_config.yml` pins minima to a specific upstream commit, so an upstream change cannot alter the live site unannounced. To pick up newer theme changes, replace the commit hash with a recent one from <https://github.com/jekyll/minima/commits/master>, push, and check the site still renders; the overridden head, header, footer, home and post files in `_includes/` and `_layouts/` were copied from that commit and may need the same update.
