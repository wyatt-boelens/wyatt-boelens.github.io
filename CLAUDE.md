# wyatt-boelens.github.io

Wyatt Boelens's public GTM/RevOps systems portfolio, hosted on GitHub Pages. **This repository is public** — nothing confidential goes in it.

## What this is

A collection of case studies demonstrating GTM systems design and AI-agent-building skills, aimed at RevOps / GTM-systems hiring managers. Each case study is a standalone HTML file. `index.html` is the homepage and links to all of them.

## CRITICAL — read before adding or editing anything

Everything in this repo is genericized and fictional on purpose: fictional company names, fictional brand rosters, fictional prospect data. The real, confidential business logic these case studies are based on (real SubSuite client/brand data, real classification rules tied to actual business context) lives in a **separate, personal, non-project Claude Code skills location** — never inside this repository. Before adding any new content here:

- Never paste in real client names, real brand rosters, or real business-specific logic from Wyatt's actual SubSuite work.
- Always use fictional companies/data, consistent with the existing case studies (see below).
- If you're ever asked to "port a real skill into the portfolio," the correct move is to build a new genericized file here — not copy the real skill file in.

## Design system (keep new pages visually consistent)

All pages share one CSS design language — reuse these exact tokens for anything new:

- **Palette**: deep navy background (`#0F1B2E`), navy panels (`#152640`, `#1B3050`), amber accent (`#E3A94A`), soft blue-white text (`#EAF0F8` primary, `#93A8CC` secondary, `#5E7397` muted).
- **Fonts**: Space Grotesk (display/headings), Source Serif 4 (body text), IBM Plex Mono (labels, diagram text, technical annotations) — all loaded via Google Fonts `@import`.
- **Motif**: a faint blueprint-style grid background (`background-size:32px 32px`), amber-highlighted architecture diagrams built in inline SVG, dashed-border `.callout` boxes for honest "placeholder" or scope-limitation notes.
- **Structure per case study**: stamp/eyebrow → H1 + subhead → "the problem" → an SVG architecture diagram → numbered "architecture" rules → "why this matters" (with an honest metrics placeholder, not fabricated numbers) → "where this stops" (scope honesty) → footer.

## Existing case studies

1. **`buying-committee-router.html`** — "The Buying Committee Router." Genericized version of an ICP/persona routing skill, reframed in MEDDIC/buying-committee language (Economic Buyer, Champion, Technical Evaluator, etc.) so it reads as industry-agnostic. Includes a **live interactive demo** that calls the Claude API directly from the page (see the `<script>` block — uses `fetch` to `https://api.anthropic.com/v1/messages`, model `claude-sonnet-4-6`, `max_tokens: 1000`). Fictional company: "Northbridge."
2. **`two-speed-outreach-system.html`** — "The Two-Speed Outreach System." Genericized architecture case study (diagram + rules only, no live demo) covering a mode-gate design (fast single-touch path vs. full multi-touch campaign path), a two-layer classification approach (function vs. authority), and an honest scored comparison table of the old system vs. the new one before committing to the rebuild.
3. **`index.html`** — homepage, lists both case studies as cards linking out to the files above.

## Open items (things that still need doing, not urgent)

- Both `buying-committee-router.html` and `two-speed-outreach-system.html` have a placeholder `.callout` box under "Why this matters" — real metrics (volume processed, time saved, reply-rate deltas) should replace these once Wyatt has real numbers. Don't fabricate numbers to fill them.
- Two more case studies were discussed but not yet built: one for a "brand activation" workflow skill, and one for a "persona DNA" messaging-psychology skill. Both would need the same genericization treatment as the two above before going in this repo.

## Working conventions

- One HTML file per case study, kebab-case filename, added as a new card in `index.html` when created.
- Single-file HTML (CSS and JS inline, no build step, no external dependencies beyond Google Fonts and, for the live-demo page, the Claude API).
- Deploy is automatic via GitHub Pages once changes are pushed to `main` — no separate build/deploy command needed.
