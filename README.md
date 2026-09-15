# Open Psychological Science Nigeria — website

Source for the OPSN website: a Jekyll site built on
[Beautiful Jekyll](https://beautifuljekyll.com) with a custom OPSN theme layer.

OPSN is a community-driven initiative advancing transparent, reproducible, and
accessible psychological science in Nigeria and across Africa.

## Running it locally

```bash
bundle install
bundle exec jekyll serve
```

The site is then at `http://localhost:4000`.

## How the site is put together

| Path | What it holds |
| --- | --- |
| `index.html` | Homepage. Uses the `landing` layout for full-bleed sections. |
| `about.md`, `journal-club.md`, `resources.md`, `contact.md` | Content pages. |
| `news/index.html` | Blog index; posts live in `_posts/`. |
| `_config.yml` | Site settings, navigation, and colour tokens. |
| `assets/css/opsn.css` | The OPSN theme — palette, typography, layout. |
| `_includes/opsn-head.html` | Loads webfonts and the theme stylesheet. |
| `_layouts/landing.html` | Full-width layout used by the homepage. |

## Design

**Palette.** Forest green `#14532D` for navigation and section bands, a deeper
Nigerian-flag green `#00703C` for links, pale mint `#EAF3EC` for quiet bands and
the footer, on white.

**Type.** Playfair Display for headings, Source Serif 4 for body text.

Colour tokens are set in two places and should be kept in step: `_config.yml`
(consumed by the base Beautiful Jekyll stylesheet) and the `:root` block at the
top of `assets/css/opsn.css`.

## Adding a page

Create a markdown file in the repository root with front matter:

```yaml
---
layout: page
title: Your page title
subtitle: One line describing the page
---
```

Then add it to `navbar-links` in `_config.yml` if it should appear in the
navigation.

## Adding a news post

Add a file to `_posts/` named `YYYY-MM-DD-title.md`:

```yaml
---
layout: post
title: Your post title
tags: [journal-club]
---
```

## Licence

Site content is licensed CC BY-NC 4.0. The underlying Beautiful Jekyll theme is
MIT licensed — see `LICENSE`.
