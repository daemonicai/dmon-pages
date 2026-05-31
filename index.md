---
layout: home
title: dmon-pages
tagline: shared theme · jekyll remote_theme
lead: >-
  The shared GitHub Pages theme for the daemonicai family. Every project site sets
  remote_theme: daemonicai/dmon-pages and supplies only its own content — so the
  look stays consistent everywhere from a single source.
repo: daemonicai/dmon-pages
ctas:
  - { label: "View on GitHub →", href: "https://github.com/daemonicai/dmon-pages", primary: true }
  - { label: "daemonicai home", href: "https://daemonicai.github.io/" }
features:
  - icon: "◈"
    title: dmon-core
    body: A .NET-native coding agent inspired by Pi. Self-extensible via NuGet.
    href: https://daemonicai.github.io/dmon-core/
  - icon: "▮"
    title: dcli
    body: Inline terminal rendering — the Claude-Code-style CLI model as a .NET library.
    href: https://daemonicai.github.io/dcli/
  - icon: "❖"
    title: dmon-meko
    body: Durable, cross-session long-term memory for dmon, backed by Meko over MCP.
    href: https://daemonicai.github.io/dmon-meko/
  - icon: "⌕"
    title: dmon-websearch
    body: An out-of-tree web_search extension using the agent-in-a-tool pattern.
    href: https://daemonicai.github.io/dmon-websearch/
---

## Add a site

Push a `gh-pages` branch with a `_config.yml`:

```yaml
remote_theme: daemonicai/dmon-pages
baseurl: "/your-repo-name"
url: "https://daemonicai.github.io"
title: your-project
github: { owner: daemonicai, repo: your-repo-name }
plugins: [jekyll-remote-theme, jekyll-seo-tag]
defaults:
  - scope: { path: "" }
    values: { layout: home }
```

…and an `index.md` whose front matter drives the hero, badges, and feature grid
(`title`, `tagline`, `lead`, `repo`, `nuget`, `features`). The
[README](https://github.com/daemonicai/dmon-pages#readme) has the full template.

Edit the theme here once, and every site picks up the change on its next build.
