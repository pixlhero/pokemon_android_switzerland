# Project: Pokémon Android Switzerland

Investigation site documenting Pokémon games missing from Google Play in Switzerland.

## Structure

- `docs/index.html` — Single-file static site (HTML + CSS + JS all inline). This is the only content file.
- Hosted via GitHub Pages from the `develop` branch, `/docs` folder.
- Default branch is `develop` (not `main`).

## Site architecture

- Everything lives in one HTML file: styles in `<style>`, content in `<body>`, translations and logic in `<script>`.
- i18n: Two languages (EN/DE). Translations are in JS objects (`en` and `de`) keyed by `data-i18n` attribute values. When adding new translatable text, add the key to both language objects.
- Design system uses CSS custom properties defined in `:root` (warm paper palette: `--bg`, `--surface`, `--raised`, `--border`, `--text`, `--text-2`, `--muted`, and Pokémon red `--accent` as the only accent).
- Fonts: Fredoka (headings, figures, stamps) and Nunito (body, meta) loaded from Google Fonts.

## Key sections in index.html

- Hero (landing)
- Affected Games grid
- Replies Received — collapsible `.email` cards rendered from `REPLIES` (default closed)
- Possible Reasons
- Actions Taken & Next Steps (progress checklists)
- Contact List (tables)

## Workflow

- After making any changes, always commit and push to `develop` immediately. The site is live on GitHub Pages and users depend on it being up to date.

## Style notes

- Warm case-file aesthetic (paper and brown ink). Avoid blue tints. Red is used sparingly: the stamp, the key figure, focus.
- Signature detail: the rotated `.stamp` ("Missing", "Confirmed", "Non-answer"). It is always rendered from data, never added as decoration.
- No glows, gradients, pill-shaped everything, uppercase tracked labels, emoji icons or scroll-reveal animations.
