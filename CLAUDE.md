# Project: Pokémon Android Switzerland

Investigation site documenting Pokémon games missing from Google Play in Switzerland.

## Structure

- `docs/index.html` — Single-file static site (HTML + CSS + JS all inline). This is the only content file.
- Hosted via GitHub Pages from the `develop` branch, `/docs` folder.
- Default branch is `develop` (not `main`).

## Site architecture

- Everything lives in one HTML file: styles in `<style>`, content in `<body>`, translations and logic in `<script>`.
- i18n: Two languages (EN/DE). Translations are in JS objects (`en` and `de`) keyed by `data-i18n` attribute values. When adding new translatable text, add the key to both language objects.
- Design system uses CSS custom properties defined in `:root` (warm cream/brown palette: `--bg`, `--surface`, `--border`, `--accent`, `--text`, `--muted`, etc.).
- Fonts: Fredoka (headings/body) and Nunito (mono/meta text) loaded from Google Fonts.

## Key sections in index.html

- Hero (landing)
- Affected Games grid
- Replies Received — collapsible envelope-style `<details>` elements (default closed)
- Possible Reasons
- Actions Taken & Next Steps (progress checklists)
- Contact List (tables)

## Workflow

- After making any changes, always commit and push to `develop` immediately. The site is live on GitHub Pages and users depend on it being up to date.

## Style notes

- Warm, friendly aesthetic (cream/brown/gold tones). Avoid blue tints in content areas.
- The envelope UI for replies uses `<details class="envelope">` with a stamp icon, sender info, and verdict preview when closed.
