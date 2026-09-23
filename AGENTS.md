# Documentation project instructions

## About this project

- Public documentation for Crossword, built on [Mintlify](https://mintlify.com).
- Pages are MDX files with YAML frontmatter.
- Site configuration lives in `docs.json`.
- A page is only visible once its path is listed in `navigation` in `docs.json`.
- Run `mint validate` and `mint broken-links` before opening a PR.

## Terminology

- The product is **Crossword**. Never "CometChat AI", never "the platform".
- A reusable collection of contextual behaviors is a **Journey**. Never "Playbook".
- {/* TODO: add product-specific terms and preferred usage as they settle */}

## Style preferences

- Active voice, second person ("you").
- One idea per sentence.
- Sentence case for headings.
- Bold for UI elements: Click **Settings**.
- Code formatting for file names, commands, paths, and code references.
- No em dashes.
- Prices and amounts in US dollars ($), never rupees or other currencies.

## Content boundaries

- This repo is **public**. Everything committed here is world-readable.
- Do not document internal-only admin surfaces, staff tooling, or infrastructure.
- Never commit API keys, tokens, workspace keys tied to real customers, or
  internal hostnames that are not already public.
- Architecture decisions, ADRs, RFCs and runbooks belong in the private product
  repo, not here.
- Never use real customer, merchant, or brand names in examples. Use generic
  stand-ins such as "your storefront", "a sneaker brand", or "Product A".
