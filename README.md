# dmon-pages

**Shared GitHub Pages theme for the [daemonicai](https://github.com/daemonicai) project family.**

This repo is a Jekyll [remote theme](https://github.com/benbalter/jekyll-remote-theme).
Every project site in the org references it so they all share one look from a single
source of truth. Edit the theme here, and every site picks up the change on its next build.

Live hub: **https://daemonicai.github.io/dmon-pages/**

## What's in here

```
_layouts/
  default.html      # HTML shell: head, header, content, footer
  home.html         # project landing layout (hero + badges + features + prose)
_includes/
  head.html         # meta, SEO, favicon, stylesheet link
  header.html       # sticky nav with the family links (single source)
  footer.html       # cross-links every family site together
_sass/
  dmon.scss         # the entire visual theme (dark, terminal-inspired)
assets/css/
  style.scss        # entry point — pulls in _sass/dmon.scss
index.md            # this repo's own hub page
```

## Use it from another repo

Add a `gh-pages` branch (or a `docs/` folder) with a `_config.yml`:

```yaml
remote_theme: daemonicai/dmon-pages
baseurl: "/your-repo-name"          # project pages are served under /<repo>
url: "https://daemonicai.github.io"
title: your-project
github:
  owner: daemonicai
  repo: your-repo-name
plugins:
  - jekyll-remote-theme
  - jekyll-seo-tag
defaults:
  - scope: { path: "" }
    values: { layout: home }
```

Then an `index.md` supplies the content via front matter:

```yaml
---
layout: home
title: your-project
tagline: one-line kicker
lead: A sentence or two for the hero.
repo: daemonicai/your-repo-name     # drives the GitHub button + stars/license badges
nuget: your-package-id              # optional — drives the NuGet button + version badges
features:
  - { icon: "◈", title: "Feature", body: "What it does." }
---

Markdown body renders below the hero.
```

Enable Pages for the repo (Settings → Pages → Source: `gh-pages` branch) and the site
appears at `https://daemonicai.github.io/your-repo-name/`.

## Local preview

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000/dmon-pages/
```

## The family

| Site | Repo | What |
|------|------|------|
| [dmon-core](https://daemonicai.github.io/dmon-core/) | `dmon-core` | the .NET-native agent core |
| [dcli](https://daemonicai.github.io/dcli/) | `dcli` | inline terminal-rendering library |
| [dmon-meko](https://daemonicai.github.io/dmon-meko/) | `dmon-meko` | long-term memory over Meko |
| [dmon-websearch](https://daemonicai.github.io/dmon-websearch/) | `dmon-websearch` | web_search extension |
