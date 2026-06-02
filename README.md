# RevenueBase Design System

A `design.md`-format design system for [RevenueBase](https://revenuebase.ai), covering both the **marketing site** and the **product app**, in **light and dark** themes.

- **[DESIGN.md](DESIGN.md)** — the system itself (YAML tokens + token-referenced prose), in the [VoltAgent / Google `design.md`](https://github.com/VoltAgent/awesome-design-md) format. Lint with `npx @google/design.md lint DESIGN.md`.

## Identity at a glance

- **Color** — Navy (primary brand), Amber/Gold (signature accent, logo only), Teal (action), Slate (neutral text).
- **Shape** — Square. 0px everywhere; 8px only on the floating nav. Crosshair corner-marks, a 45px hairline grid, and a 4% noise grain are the blueprint motifs.
- **Type** — DM Sans (headlines + UI), Fraunces (italic accents + product page titles), JetBrains Mono (eyebrows + code).
- **Themes** — Light (`#f1f4f9` canvas) and Dark (`#0e1a2e` canvas); both navy-tinted, never pure white/black.
- **Two surfaces** — Marketing runs navy text / 16px / muted primary; Product runs slate text / 14px / solid-navy primary + teal action.

## Review scaffold

These interactive pages were built to review the system step by step; open any in a browser:

- `foundations.html` — color, themes, type, spacing, shape, texture
- `marketing.html` — the 11 marketing components
- `product.html` — the product app components

Each has a live light/dark toggle and renders in the real fonts and tokens.

## Assets

- `assets/bg-noise-light.webp`, `assets/bg-noise-dark.webp` — the 256px noise grain (use at 4%).
- `assets/grid-light.svg`, `assets/grid-dark.svg` — the 45px hairline grid tile.

## Sources

Extracted from the live site (revenuebase.ai, computed CSS in both themes) and the Phase-1 Figma product file (node geometry, fills, and type).
