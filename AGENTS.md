<!-- gitbook-agent-instructions:start -->

## GitBook Documentation Editing

This repository contains documentation synced with GitBook via Git Sync.

Before editing GitBook-synced Markdown, YAML, or asset files, make sure the GitBook skill is available and up to date in your local agent environment. Prefer installing or updating it with:

```bash
npx skills add gitbookio/gitbook-skills
```

This command may add or update local agent skill files. Use them only as local agent instructions; do not commit those installed skill files or any tool-generated agent configuration unless the user explicitly asks for it.

If `npx` is unavailable, load the skill from:

https://gitbook.com/docs/skill.md

When making changes, preserve GitBook sync metadata such as frontmatter, `SUMMARY.md`, `docs.yaml`, `.gitbook/`, and asset links unless the requested edit explicitly requires changing them.

<!-- gitbook-agent-instructions:end -->

# Repository Context

This repository is the source for **HSON Market Reading System**, an advanced
crypto market-reading and trade-execution course published at
<https://hson.gitbook.io/hson-docs>. The GitBook-synced source of truth lives in
`public/`; the root `README.md` is the GitHub-facing project introduction.

## Repository Contents

- `public/README.md` is the GitBook landing page and course overview.
- `public/SUMMARY.md` defines the published navigation and page order.
- `public/01-foundations/` through `public/09-quotes/` contain the curriculum.
- `public/.gitbook/assets/diagrams/` contains the SVG diagrams referenced by
  course pages.
- `assets/logo.png` is a repository-level brand asset and is not currently
  referenced by the GitBook pages.
- `public/core-concepts/`, `public/getting-started/`, `public/guides/`, and
  `public/reference/` are empty legacy directories and are not in the current
  navigation.

The curriculum is organized as follows:

1. Foundations: market mechanics and the trading decision hierarchy.
2. Price Action: structure, liquidity, acceptance, and rejection.
3. Auction Market Theory: balance, value, profile references, and failed
   auctions.
4. Order Flow: bid/ask delta, absorption, exhaustion, trapped traders, and CVD.
5. Trading Playbook: failed-auction reversal, breakout acceptance, and trend
   pullback setups.
6. Execution Framework: entry, invalidation, targets, and management.
7. Checklists: pre-market, pre-trade, and post-trade review.
8. Rules: the "Make it stop me out" execution rule.
9. Quotes: researched trading maxims translated into operational rules.

## Current Progress

Snapshot as of 2026-08-28:

- The navigated course contains 28 curriculum pages across nine modules, plus
  the GitBook landing page.
- All pages listed in `public/SUMMARY.md` exist; no TODO, TBD, FIXME, WIP, draft,
  or placeholder markers are present in the repository content.
- Ten SVG diagrams support the course and are used in 15 page placements.
- The latest completed work added the Rules module and corrected the HVN/LVN
  volume-profile illustration.
- Repository housekeeping now ignores macOS `.DS_Store` files and no longer
  tracks the previously committed root copy.
- The Quotes module now begins with a researched treatment of “It’s okay to be
  wrong; it’s not okay to stay wrong.”

## Pending Work

- Confirm the GitBook deployment reflects the latest Quotes and repository
  housekeeping changes.
- Decide whether `assets/logo.png` should be wired into the repository README,
  GitBook customization, or both.

Update both **Current Progress** and **Pending Work** after every repository work
session. Record completed items in Current Progress, remove them from Pending
Work, and add any newly discovered follow-ups before handing work back to the
user. Keep the snapshot date current whenever either section changes.

## Editing Notes

- Keep `public/SUMMARY.md` synchronized whenever pages are added, removed,
  renamed, or reordered.
- Preserve each page's YAML frontmatter and GitBook block syntax.
- Keep diagram paths relative to the page and store GitBook diagrams under
  `public/.gitbook/assets/diagrams/`.
- Do not add content to the empty legacy directories unless the requested
  information architecture explicitly restores them.
- Do not commit locally installed agent skills or generated agent configuration.
