---
layout: home
title: daemonicai
tagline: open source · .NET 10
lead: >-
  .NET-native tooling for building coding agents — a self-extensible agent core,
  the terminal UI behind it, durable memory, and provider-grounded extensions.
ctas:
  - label: Browse the org →
    href: https://github.com/daemonicai
    primary: true
  - label: dmon, the agent core
    href: https://daemonicai.github.io/dmon-core/
features:
  - icon: "◈"
    title: dmon-core
    body: A .NET-native coding agent inspired by Pi. Self-extensible via NuGet, JSONL/stdio RPC, conservative permissions.
    href: https://daemonicai.github.io/dmon-core/
  - icon: "▮"
    title: dcli
    body: Inline terminal rendering — the Claude-Code-style CLI model as a reusable .NET library.
    href: https://daemonicai.github.io/dcli/
  - icon: "❖"
    title: dmon-meko
    body: Durable, cross-session long-term memory for dmon, backed by Meko over MCP.
    href: https://daemonicai.github.io/dmon-meko/
  - icon: "⌕"
    title: dmon-websearch
    body: An out-of-tree web_search extension using the agent-in-a-tool pattern with provider-grounded search.
    href: https://daemonicai.github.io/dmon-websearch/
---

## One stack, many pieces

The **daemonicai** projects are built to fit together. `dmon-core` is the agent;
`dcli` renders its terminal surface; `dmon-meko` gives it memory; `dmon-websearch`
is the reference out-of-tree extension. Each ships independently on NuGet, and each
site you're looking at shares this one theme.

## About this repo

`dmon-pages` is the shared Jekyll **remote theme** for the whole family. Every
project site sets `remote_theme: daemonicai/dmon-pages` and supplies only its own
content — so the look stays consistent everywhere from a single source. See the
[README](https://github.com/daemonicai/dmon-pages#readme) for how to add a new site.
