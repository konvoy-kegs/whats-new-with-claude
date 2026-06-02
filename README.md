# What's New with Claude?

A live, daily-refreshed digest of releases, features, and community content across:

- **Claude Code** — CLI release notes, version reconciliation between npm, dist-tags, and the public changelog
- **Claude Desktop** — features in the macOS/Windows desktop app
- **Claude Cowork** — Cowork product updates, plugins, computer use, scheduled tasks

## How it updates

A scheduled Cowork task (`claude-code-daily-digest`) runs every weekday morning at 8am local time. Each run:

1. Pulls the newest `@anthropic-ai/claude-code` version directly from the npm registry — not just the `latest` dist-tag, because Anthropic publishes patch versions to npm before promoting the tag.
2. Fetches the public CHANGELOG.md from `anthropics/claude-code`.
3. Cross-checks against the GitHub Releases API.
4. Web-searches Anthropic blog posts and community tutorials covering Claude Code, Desktop, and Cowork.
5. Rewrites `docs/index.html` in this repo and pushes it to `main`.
6. Posts the live URL to `#cloud-engineers` in Slack.

## Live site

GitHub Pages serves the latest digest at:

**https://konvoy-kegs.github.io/whats-new-with-claude/**

## Repo layout

```
docs/
  index.html      # the live page served by GitHub Pages
```

GitHub Pages is configured to serve from `main` branch, `/docs` folder.

## Manual run

If the morning task missed (Cowork was closed at 8am), open Cowork and the task runs on next launch.
