# Crossword docs

Public documentation for [Crossword](https://crswrd.ai), built on [Mintlify](https://mintlify.com).

## Local preview

```bash
npm i -g mint
mint dev
```

Serves on http://localhost:3000 and live-reloads on save. Run it from the repo
root (the directory holding `docs.json`).

## Before you push

```bash
mint validate       # strict schema + build check, fails on warnings
mint broken-links   # internal link check
```

## How it deploys

Pushing to `main` triggers a Mintlify deploy. There is no build workflow in this
repo — deployment is handled by the Mintlify GitHub App, configured at
[app.mintlify.com](https://app.mintlify.com) under Settings → Deployment → Git
Settings.

## Layout

| Path            | What it is                                                   |
| --------------- | ------------------------------------------------------------ |
| `docs.json`     | Site config: theme, colors, navigation, navbar, footer        |
| `*.mdx`         | Pages. Path maps to URL — `guides/setup.mdx` → `/guides/setup` |
| `favicon.svg`   | **Placeholder.** Replace with the real mark                   |
| `.mintignore`   | Files Mintlify should not publish                             |
| `AGENTS.md`     | Conventions for AI agents editing these docs                  |

## Adding a page

1. Create the `.mdx` file with `title` and `description` frontmatter.
2. Add its path (without the extension) to `navigation` in `docs.json`.

A page that exists on disk but is missing from `navigation` will not appear in
the sidebar.

## Still to do

- [ ] Replace `favicon.svg` with the real mark
- [ ] Add `logo.light` / `logo.dark` SVGs and wire them into `docs.json`
- [ ] Point the docs domain (e.g. `docs.crswrd.ai`) at Mintlify
- [ ] Write the real Introduction and Quickstart
