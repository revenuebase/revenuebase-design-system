---
version: alpha
name: RevenueBase-design-analysis
description: "A square-cornered, blueprint-grade B2B data-infrastructure system spanning two surfaces (marketing site + product app) and two themes (light + dark, both navy-tinted — never pure #fff/#000). Navy (#0f537e family) is the primary brand color; amber/gold (#ffe099 / #704700) is the signature accent reserved for the logo mark and brand moments; teal (#00b5b0) is the action accent; slate is the neutral text ramp. The voice is technical and precise: every button, card, input, tag and panel is 0px (the only rounded element is the floating nav at 8px), reinforced by a hairline 45px grid, a 4% noise grain over the canvas, and crosshair corner-marks on marketing buttons and framed panels. Type is a three-family system: DM Sans carries headlines (weight 500) and all UI; Fraunces appears only as italic accent words inside headlines and for stat figures, and as the roman serif for product page titles; JetBrains Mono sets eyebrows, labels and code. The marketing surface is brand-saturated (navy text, 16px body, muted navy-150 primary button); the product surface is functional (slate text ramp, 14px body, solid navy-800 primary with teal action buttons)."

colors:
  # ---- Canonical semantic aliases ----
  primary: "#0f537e"
  on-primary: "#ffffff"
  # ---- Navy (primary brand) ----
  navy-50: "#f1f4f9"
  navy-75: "#edf3fa"
  navy-100: "#dde6f1"
  navy-150: "#c1cfe0"
  navy-200: "#b5c8e0"
  navy-300: "#89a5cc"
  navy-400: "#5e82b8"
  navy-500: "#43649f"
  navy-600: "#2e5a82"
  navy-700: "#1a4a6e"
  navy-800: "#0f537e"
  navy-850: "#0a3652"
  navy-900: "#0e1a2e"
  navy-950: "#091220"
  # ---- Amber / Gold (signature accent) ----
  amber-50: "#fff8e6"
  amber-100: "#fff0cc"
  amber-200: "#ffe099"
  amber-300: "#ffce66"
  amber-400: "#ffbb33"
  amber-500: "#ffaa00"
  amber-600: "#bf7c00"
  amber-700: "#946000"
  amber-800: "#704700"
  amber-900: "#4d3000"
  # ---- Teal (action accent) ----
  teal-50: "#ecfcfb"
  teal-100: "#cff5f4"
  teal-200: "#9eeae7"
  teal-300: "#62dad6"
  teal-400: "#2dc9c4"
  teal-500: "#00b5b0"
  teal-600: "#219f98"
  teal-700: "#107069"
  teal-800: "#0a5551"
  teal-900: "#063d3b"
  # ---- Slate (neutral text & dividers) ----
  slate-50: "#f7f7f9"
  slate-100: "#ecedf0"
  slate-200: "#d2d5dc"
  slate-300: "#adb2bd"
  slate-400: "#868c9b"
  slate-500: "#626879"
  slate-600: "#444a58"
  slate-700: "#2e323d"
  slate-800: "#1e2129"
  slate-900: "#13161d"
  slate-950: "#0b0d11"
  # ---- Semantic ----
  success: "#2e7d32"
  success-bg: "#e6f3e6"
  danger: "#c62828"
  danger-bg: "#fae3e3"
  warning: "#bf7c00"
  warning-bg: "#fff8e6"
  info: "#0f537e"
  # ---- Comparison (marketing before/after) ----
  comparison-negative: "#c9413a"
  comparison-negative-bg: "#f2dcdd"
  comparison-positive: "#1a9e6f"
  comparison-positive-bg: "#d9eae4"
  # ---- Logo gradient ----
  logo-gradient-from: "#ff7708"
  logo-gradient-to: "#ffaa00"

typography:
  display:
    fontFamily: DM Sans
    fontSize: 54px
    fontWeight: 500
    lineHeight: 1.08
    letterSpacing: -1.6px
  display-accent:
    fontFamily: Fraunces
    fontStyle: italic
    fontSize: 58px
    fontWeight: 400
    lineHeight: 1.05
    letterSpacing: -1.0px
  h1:
    fontFamily: DM Sans
    fontSize: 46px
    fontWeight: 500
    lineHeight: 1.10
    letterSpacing: -1.4px
  h2:
    fontFamily: DM Sans
    fontSize: 40px
    fontWeight: 500
    lineHeight: 1.10
    letterSpacing: -1.2px
  h3:
    fontFamily: DM Sans
    fontSize: 30px
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: -0.6px
  title-serif:
    fontFamily: Fraunces
    fontSize: 26px
    fontWeight: 600
    lineHeight: 1.12
    letterSpacing: -0.3px
  card-title:
    fontFamily: DM Sans
    fontSize: 19px
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: -0.2px
  body-lg:
    fontFamily: DM Sans
    fontSize: 20px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: 0
  body:
    fontFamily: DM Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: 0
  body-sm:
    fontFamily: DM Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: 0
  eyebrow:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.30
    letterSpacing: 0.8px
    textTransform: uppercase
  label:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: 500
    lineHeight: 1.30
    letterSpacing: 1.0px
    textTransform: uppercase
  button:
    fontFamily: DM Sans
    fontSize: 15px
    fontWeight: 500
    lineHeight: 1.0
    letterSpacing: 0
  stat-figure:
    fontFamily: Fraunces
    fontStyle: italic
    fontSize: 52px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: -0.5px
  mono:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: 0

rounded:
  sharp: 0px
  nav: 8px
  pill: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  xxxl: 64px
  section-sm: 80px
  section: 112px
  section-lg: 160px
  section-top: 224px

components:
  # ============ SHARED ============
  button-primary-marketing:
    backgroundColor: "{colors.navy-150}"
    textColor: "{colors.navy-800}"
    typography: "{typography.button}"
    rounded: "{rounded.sharp}"
    padding: 15px 24px
  button-secondary:
    backgroundColor: transparent
    textColor: "{colors.navy-800}"
    typography: "{typography.button}"
    rounded: "{rounded.sharp}"
    padding: 15px 24px
  nav-button:
    backgroundColor: "{colors.navy-150}"
    textColor: "{colors.navy-800}"
    typography: "{typography.button}"
    rounded: "{rounded.nav}"
    padding: 10px 16px
  crosshair-corner:
    backgroundColor: "{colors.navy-800}"
    textColor: "{colors.navy-800}"
    typography: "{typography.label}"
    rounded: "{rounded.sharp}"
    padding: 0px
  # ============ MARKETING ============
  top-nav:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.nav}"
    padding: 14px 22px
  hero:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.display}"
    rounded: "{rounded.sharp}"
    padding: 96px 0px
  eyebrow:
    backgroundColor: transparent
    textColor: "{colors.navy-800}"
    typography: "{typography.eyebrow}"
    rounded: "{rounded.sharp}"
    padding: 0px
  feature-card:
    backgroundColor: "{colors.teal-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 26px
  stat-figure:
    backgroundColor: transparent
    textColor: "{colors.navy-800}"
    typography: "{typography.stat-figure}"
    rounded: "{rounded.sharp}"
    padding: 0px
  logo-tile:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.card-title}"
    rounded: "{rounded.sharp}"
    padding: 0px
  testimonial-tag:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 3px 9px
  testimonial-card:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.title-serif}"
    rounded: "{rounded.sharp}"
    padding: 32px
  comparison-row-negative:
    backgroundColor: "{colors.comparison-negative-bg}"
    textColor: "{colors.comparison-negative}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 9px 0px
  comparison-row-positive:
    backgroundColor: "{colors.comparison-positive-bg}"
    textColor: "{colors.comparison-positive}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 9px 0px
  faq-row:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.card-title}"
    rounded: "{rounded.sharp}"
    padding: 18px 4px
  cta-banner:
    backgroundColor: "{colors.navy-900}"
    textColor: "{colors.navy-50}"
    typography: "{typography.display}"
    rounded: "{rounded.sharp}"
    padding: 72px
  footer:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body}"
    rounded: "{rounded.sharp}"
    padding: 40px
  # ============ PRODUCT ============
  app-sidebar:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-700}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 16px 0px
  nav-item:
    backgroundColor: transparent
    textColor: "{colors.slate-700}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 9px 18px
  nav-item-active:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 9px 18px
  app-top-bar:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-700}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 13px 24px
  credits-pill:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 6px 13px
  page-title:
    backgroundColor: transparent
    textColor: "{colors.slate-900}"
    typography: "{typography.title-serif}"
    rounded: "{rounded.sharp}"
    padding: 0px
  tabs:
    backgroundColor: transparent
    textColor: "{colors.slate-400}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 11px 2px
  tab-active:
    backgroundColor: transparent
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 11px 2px
  button-primary-product:
    backgroundColor: "{colors.navy-800}"
    textColor: "#ffffff"
    typography: "{typography.button}"
    rounded: "{rounded.sharp}"
    padding: 11px 18px
  button-action:
    backgroundColor: "{colors.teal-500}"
    textColor: "#ffffff"
    typography: "{typography.button}"
    rounded: "{rounded.sharp}"
    padding: 11px 18px
  button-destructive:
    backgroundColor: "{colors.danger-bg}"
    textColor: "{colors.danger}"
    typography: "{typography.button}"
    rounded: "{rounded.sharp}"
    padding: 11px 18px
  plan-card:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-900}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 20px
  plan-card-featured:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-900}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 20px
  badge-success:
    backgroundColor: "{colors.success-bg}"
    textColor: "{colors.success}"
    typography: "{typography.label}"
    rounded: "{rounded.sharp}"
    padding: 3px 9px
  badge-neutral:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.label}"
    rounded: "{rounded.sharp}"
    padding: 3px 9px
  badge-popular:
    backgroundColor: "{colors.navy-800}"
    textColor: "#ffffff"
    typography: "{typography.label}"
    rounded: "{rounded.sharp}"
    padding: 3px 9px
  data-table-header:
    backgroundColor: "{colors.slate-50}"
    textColor: "{colors.slate-400}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 11px 16px
  data-table-cell:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-700}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 12px 16px
  metric-panel:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-900}"
    typography: "{typography.h2}"
    rounded: "{rounded.sharp}"
    padding: 20px
  progress-stepper:
    backgroundColor: "{colors.slate-50}"
    textColor: "{colors.slate-700}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 16px 18px
  step-chip-done:
    backgroundColor: "#ffffff"
    textColor: "{colors.teal-700}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 9px 12px
  numbered-step-active:
    backgroundColor: "{colors.navy-800}"
    textColor: "#ffffff"
    typography: "{typography.body-sm}"
    rounded: "{rounded.pill}"
    padding: 0px
  text-input:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-900}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 11px 13px
  segmented-control:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-400}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 9px 16px
  segmented-control-active:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 9px 16px
  option-card:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-700}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 20px
  option-card-selected:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 20px
  dropzone:
    backgroundColor: "{colors.slate-50}"
    textColor: "{colors.slate-400}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 30px
  saved-card-row:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-900}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 13px 16px
  banner-warning:
    backgroundColor: "{colors.warning-bg}"
    textColor: "{colors.amber-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 13px 16px
  banner-info:
    backgroundColor: "{colors.navy-50}"
    textColor: "{colors.navy-800}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 13px 16px
  result-valid:
    backgroundColor: "{colors.success-bg}"
    textColor: "{colors.success}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 13px 16px
  result-invalid:
    backgroundColor: "{colors.danger-bg}"
    textColor: "{colors.danger}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 13px 16px
  result-unknown:
    backgroundColor: "{colors.slate-50}"
    textColor: "{colors.slate-500}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 13px 16px
  integration-row:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-900}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 16px
  modal:
    backgroundColor: "#ffffff"
    textColor: "{colors.slate-900}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sharp}"
    padding: 0px
---

## Overview

RevenueBase is a B2B data-infrastructure brand, and its design system reads like infrastructure: square, precise, technical, quietly confident. Two surfaces share one foundation — a **marketing site** (revenuebase.ai) and a **product app** (the dashboard) — and both ship **light and dark themes**. Neither theme uses pure white or black: light canvas is `{colors.navy-50}` (#f1f4f9), dark canvas is `{colors.navy-900}` (#0e1a2e). Everything is navy-tinted.

The palette is four ramps. **Navy** (`{colors.navy-800}` #0f537e at its core) is the primary brand color and carries text and interactive states. **Amber/Gold** (`{colors.amber-200}` / `{colors.amber-800}`) is the signature accent — it lives in the logo mark and brand moments only, never as a button or large fill. **Teal** (`{colors.teal-500}` #00b5b0) is the action accent — progress indicators, checks, and the product's in-app action buttons. **Slate** is the neutral ramp that carries the product's text hierarchy.

The defining shape decision is that **the whole system is square** — 0px corners on buttons, inputs, cards, tags, and panels, on both the site and the app. The Figma product file contains no rounded node anywhere. The only rounded element is the floating nav bar at `{rounded.nav}` 8px. Three motifs reinforce the blueprint feel: a **45px hairline grid** on framed surfaces, a **4% noise grain** over the canvas, and **crosshair corner-marks** (the site's `c-crosshair` element) at the corners of marketing buttons and framed panels.

Type is a three-family system used differently per surface. **DM Sans** carries headlines (weight 500) and all UI. **Fraunces** appears only as *italic accent words* inside marketing headlines and for stat figures, and as the *roman serif* for product page titles — it never sets a full marketing headline. **JetBrains Mono** sets eyebrows, micro-labels, and code.

**Key Characteristics:**
- **Dual-theme, dual-surface** — light + dark, marketing + product, on one token foundation.
- **Square by default** — 0px everywhere; `{rounded.nav}` 8px is the single exception.
- **Navy primary, amber accent, teal action** — three distinct color jobs; amber is scarce.
- **Two text ramps** — marketing runs on navy, product runs on slate.
- **DM Sans headlines + Fraunces-italic accents** — the serif is an accent, not a display face (except product page titles).
- **Crosshair corners, hairline grid, 4% noise** — the blueprint/infrastructure signal.
- The marketing primary CTA is deliberately **quiet** (`{colors.navy-150}` muted fill); the product primary is **solid** (`{colors.navy-800}`).

## Colors

> Source: revenuebase.ai (light + dark, computed CSS variables) and the Phase-1 Figma product file (node fills).

### Brand & Accent
- **Navy** (`{colors.navy-800}`): Primary brand. Marketing text, product interactive states, links, prices.
- **Amber/Gold** (`{colors.amber-200}` fill / `{colors.amber-800}` text): Signature accent. Logo mark and brand moments only.
- **Teal** (`{colors.teal-500}`): Action accent. Progress bars, checks, product action buttons.
- **Logo gradient** (`{colors.logo-gradient-from}` → `{colors.logo-gradient-to}`): The chevron mark only.

### Neutral (Slate)
- **Slate ramp** (`{colors.slate-900}` → `{colors.slate-400}`): The product's text hierarchy and dividers — heading `{colors.slate-900}`, body `{colors.slate-700}`, muted `{colors.slate-400}`, disabled `{colors.slate-300}`.

### Semantic
- **Success** (`{colors.success}` on `{colors.success-bg}`): Active / Free badges, valid results, positive deltas.
- **Danger** (`{colors.danger}` on `{colors.danger-bg}`): Cancel, sign out, negative credit values, invalid results.
- **Warning** (`{colors.warning}` on `{colors.warning-bg}`): Alert banners (e.g. "Integrations cannot be modified once configured").
- **Info** (`{colors.info}`): Informational callouts, links, emphasis.
- **Comparison** (`{colors.comparison-negative}` / `{colors.comparison-positive}`): The marketing before/after section's red-vs-green bullets.

### Light Theme
| Role | Token |
|---|---|
| canvas | `{colors.navy-50}` |
| surface | `#ffffff` / `{colors.navy-100}` |
| text-primary | `{colors.navy-800}` (marketing) · `{colors.slate-900}` (product) |
| text-secondary | navy-800 @72% · `{colors.slate-700}` (product) |
| text-muted | navy-800 @45% · `{colors.slate-400}` (product) |
| border | `{colors.navy-200}` · `{colors.slate-200}` (product) |
| brand accent | `{colors.amber-100}` bg / `{colors.amber-800}` text |
| action | `{colors.teal-500}` |

### Dark Theme
| Role | Token |
|---|---|
| canvas | `{colors.navy-900}` |
| surface | `{colors.navy-850}` / `{colors.navy-800}` |
| text-primary | `{colors.navy-50}` |
| text-secondary | `{colors.navy-200}` |
| text-muted | `{colors.navy-300}` |
| border | `{colors.navy-700}` |
| brand accent | `{colors.amber-900}` bg / `{colors.amber-50}` text |
| action | `{colors.teal-400}` |

## Typography

### Font Families
- **DM Sans** — headlines (weight 500) and all UI, body, buttons, nav. Fallback `Arial, sans-serif`.
- **Fraunces** — italic accent words inside marketing headlines (`{typography.display-accent}`), stat figures (`{typography.stat-figure}`), and roman product page titles (`{typography.title-serif}`). Fallback `Georgia, serif`.
- **JetBrains Mono** — eyebrows (`{typography.eyebrow}`), micro-labels (`{typography.label}`), and code (`{typography.mono}`). Fallback `Menlo, monospace`.

### Hierarchy

| Token | Family | Size | Weight | Use |
|---|---|---|---|---|
| `{typography.display}` | DM Sans | 54px | 500 | Marketing hero headline |
| `{typography.display-accent}` | Fraunces italic | 58px | 400 | Italic accent words in hero |
| `{typography.h1}` | DM Sans | 46px | 500 | Section headlines |
| `{typography.h2}` | DM Sans | 40px | 500 | Sub-section headlines, CTA |
| `{typography.h3}` | DM Sans | 30px | 500 | Smaller headlines |
| `{typography.title-serif}` | Fraunces | 26px | 600 | **Product page titles** (roman serif) |
| `{typography.card-title}` | DM Sans | 19px | 600 | Card titles, FAQ questions |
| `{typography.body-lg}` | DM Sans | 20px | 400 | Lead paragraphs |
| `{typography.body}` | DM Sans | 16px | 400 | Marketing body |
| `{typography.body-sm}` | DM Sans | 14px | 400 | **Product UI base**, captions |
| `{typography.eyebrow}` | JetBrains Mono | 13px | 500 | Section eyebrows (uppercase) |
| `{typography.label}` | JetBrains Mono | 11px | 500 | Stat labels, badges (uppercase) |
| `{typography.button}` | DM Sans | 15px | 500 | Button labels |
| `{typography.stat-figure}` | Fraunces italic | 52px | 400 | Stat numerals ("1B+") |
| `{typography.mono}` | JetBrains Mono | 13px | 400 | Code, account IDs |

### Principles
- **The headline rule:** a marketing headline is DM Sans 500 with one or two words swapped to Fraunces italic at ~1.07× size — e.g. "The trust layer *for B2B data.*" The serif is the accent, never the whole line.
- **Product titles invert that:** page titles like "Data Catalog" / "Plan & Billing" are set in roman Fraunces (`{typography.title-serif}`).
- **Negative tracking on display** (-1.6px at 54px); body holds at 0.
- **Mono is always uppercase** for eyebrows and labels.
- **Two body sizes:** marketing leads with `{typography.body}` 16px; the denser product UI uses `{typography.body-sm}` 14px as its base.

### Note on Fonts
DM Sans, Fraunces, and JetBrains Mono are all open-source (Google Fonts) — these are the brand's actual faces, no substitution needed. Fraunces should be loaded with its optical-size axis and an italic cut.

## Layout

### Spacing System
- **Base unit:** 4px.
- **Tokens:** `{spacing.xxs}` 4 · `{spacing.xs}` 8 · `{spacing.sm}` 12 · `{spacing.md}` 16 · `{spacing.lg}` 24 · `{spacing.xl}` 32 · `{spacing.xxl}` 48 · `{spacing.xxxl}` 64 · `{spacing.section-sm}` 80 · `{spacing.section}` 112 · `{spacing.section-lg}` 160 · `{spacing.section-top}` 224.
- Card interior padding: `{spacing.lg}` 24px (marketing), 20px (product panels).
- Section rhythm: `{spacing.section}` 112px between marketing sections.

### Grid & Container
- Marketing max content width ~1440px; 12-column grid.
- Product app: fixed 232px sidebar + fluid content area.
- Card grids are 3-up at desktop, collapsing to 1-up on mobile.

### Whitespace Philosophy
Sections are separated by the navy-tinted canvas and hairline rules, not heavy shadow. The 45px grid and 4% grain give large empty areas texture without clutter.

## Elevation & Depth

| Level | Treatment | Use |
|---|---|---|
| 0 (flat) | No shadow, no border | Body type, hero text |
| 1 (hairline) | 1px `{colors.slate-200}` / `{colors.navy-200}` border | Default cards, panels, inputs |
| 2 (tint lift) | `{colors.navy-50}` / `{colors.slate-50}` fill on canvas | Active nav, segmented selection, table header |
| 3 (modal) | `#ffffff` surface + scrim + soft drop shadow | Dialogs only — the one place shadow appears |

Depth is carried by hairline borders and surface tints, not shadow. The only real shadow in the system is under a `{components.modal}` over its scrim.

## Shapes

### Corner Radius
| Token | Value | Use |
|---|---|---|
| `{rounded.sharp}` | 0px | **Default** — buttons, inputs, cards, tags, panels, badges |
| `{rounded.nav}` | 8px | The floating nav bar — the only rounded element |
| `{rounded.pill}` | 9999px | Reserved; only the numbered-stepper node circle uses it |

### Signature Motifs
- **Crosshair corners** (`{components.crosshair-corner}`): small `+` marks just outside the corners of marketing buttons and framed panels. The site renders them as a real `c-crosshair` element; they animate on hover/focus. **Marketing only** — not used in-product.
- **Hairline grid:** a 45px tile with a 0.5px stroke (`{colors.slate-200}` light / `{colors.navy-850}` dark) on framed surfaces (logo grid, comparison panels).
- **Noise grain:** a 256px-tiled noise texture at **4% opacity** over the canvas in both themes (light and dark assets). Felt, not seen.

## Components

### Marketing — Buttons
**`button-primary-marketing`** — the quiet CTA. `{colors.navy-150}` muted fill, `{colors.navy-800}` text, 1px `{colors.navy-300}` border, `{rounded.sharp}`, with crosshair corners. Deliberately low-contrast — not a saturated button.
**`button-secondary`** — transparent fill, `{colors.navy-800}` text, 1px border, crosshair corners.
**`nav-button`** — the one `{rounded.nav}` 8px element; muted navy fill, sits in the top nav.

### Marketing — Sections
**`top-nav`** — 8px bar, logo left, links center, "Log in" text + `nav-button` right.
**`hero`** — `{typography.eyebrow}` label, DM Sans 500 + Fraunces-italic headline, body, primary + secondary CTA pair.
**`feature-card`** — accent-tinted (color-50 fill + color-600 top rule); the three team cards use teal / slate / amber accents. Icon tile, `{typography.eyebrow}`, `{typography.card-title}`, body.
**`stat-figure`** — Fraunces-italic numeral (`{typography.stat-figure}`) + `{typography.label}`.
**`logo-tile`** + **`testimonial-tag`** — customer logos on the hairline grid; cells with a testimonial get an outlined `testimonial-tag`.
**`testimonial-card`** — Fraunces-italic pull quote, square avatar, name + role.
**`comparison-row-negative`** / **`comparison-row-positive`** — the before/after section; red `✕` bullets vs green `✓` bullets.
**`faq-row`** — DM Sans question + mono `+`, hairline dividers.
**`cta-banner`** — `{colors.navy-900}` panel with noise, amber eyebrow, DM Sans + Fraunces-italic headline, inverse buttons.
**`footer`** — `{typography.label}` column headings + DM Sans links on the navy-50 canvas.

### Product — Shell
**`app-sidebar`** — fixed 232px; logo, grouped nav with `{typography.label}` group headers, `nav-item` / `nav-item-active` (navy-50 tint + 2px left rule), bottom utility items + a danger "Sign out".
**`app-top-bar`** — right-aligned `credits-pill` + theme-toggle icon button.
**`page-title`** — roman Fraunces (`{typography.title-serif}`) + body-sm subhead.
**`tabs`** / **`tab-active`** — underline-active tabs (2px navy rule).

### Product — Buttons
**`button-primary-product`** — solid `{colors.navy-800}` fill, white text. The product's primary submit/confirm.
**`button-action`** — `{colors.teal-500}` fill, white text. In-context primary actions ("Add credits").
**`button-destructive`** — `{colors.danger-bg}` fill, `{colors.danger}` text ("Cancel renewal").
Link buttons: navy "Edit" / "Make default", danger-red "Remove".

### Product — Data Display
**`plan-card`** / **`plan-card-featured`** — accent top rule, stat columns, price; the featured tier gets a full navy border + `badge-popular`.
**`badge-success`** (Active/Free), **`badge-neutral`** (Default), **`badge-popular`** (Most popular).
**`data-table-header`** / **`data-table-cell`** — slate-50 header, hairline rows, negative values in `{colors.danger}`.
**`metric-panel`** — big DM Sans figure + label + action button.
**`integration-row`** — colored icon tile + name + meta + sync-status with a success dot.

### Product — Inputs & Controls
**`text-input`** — white fill, 1px `{colors.navy-300}` border, label above, optional helper + inline `{typography.mono}` code.
**`segmented-control`** / **`segmented-control-active`** — bordered segments, active gets navy-50 tint.
**`option-card`** / **`option-card-selected`** — destination/amount choosers; selected gets a full navy border.
**`dropzone`** — 1.5px dashed border, upload icon, "Choose File" secondary button.
**`saved-card-row`** — brand chip + masked number + `badge-neutral` Default + Edit/Remove links.
**`progress-stepper`** (bar + done/active chips) and the numbered horizontal stepper (`numbered-step-active` pill node).

### Product — Feedback & Overlays
**`banner-warning`** (amber) / **`banner-info`** (navy tint) — inline alerts.
**`result-valid`** / **`result-invalid`** / **`result-unknown`** — email-verification states (green / red / neutral).
**`modal`** — white surface over a navy scrim, header + close, body, footer CTA. The only component with a drop shadow.

## Do's and Don'ts

### Do
- Keep everything `{rounded.sharp}` 0px. The squareness is the brand.
- Reserve `{rounded.nav}` 8px for the floating nav bar only.
- Use amber strictly for the logo and brand moments — never a button.
- Keep the marketing primary CTA quiet (`{colors.navy-150}`); use solid `{colors.navy-800}` for the product primary.
- Write headlines in DM Sans 500 and swap one phrase to Fraunces italic.
- Set product page titles in roman Fraunces.
- Put crosshair corners on marketing buttons/panels; keep the product chrome clean.
- Keep the noise grain at 4% — felt, not seen.

### Don't
- Don't round corners (no 12px cards, no pill buttons) except the 8px nav.
- Don't use amber as a fill, button, or section background.
- Don't set a full headline in Fraunces (it's an italic accent, except product titles).
- Don't put crosshair corners in the product app.
- Don't introduce drop shadows anywhere but modals.
- Don't use pure `#ffffff`/`#000000` as a theme canvas — both modes are navy-tinted.
- Don't push the grain above ~5% or the grid onto full-page backgrounds.

## Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|---|---|---|
| Desktop-XL | 1440px | Default marketing layout |
| Desktop | 1280px | Card grids 3-up |
| Tablet | 1024px | Card grids 3-up → 2-up; product sidebar may collapse |
| Mobile-Lg | 768px | Nav → hamburger; grids → 1-up; comparison stacks |
| Mobile | 480px | Single column; `{typography.display}` scales 54 → ~32px |

### Collapsing Strategy
- **Top nav:** links collapse to a hamburger below 768px.
- **Product sidebar:** collapsible ("Collapse sidebar" control) → icon-only rail.
- **Card grids:** 3-up → 1-up below 768px.
- **Display type:** fluid `clamp()` scaling; headlines shrink ~40% to mobile.

### Touch Targets
- Buttons hold ≥40px tap height; nav items ≥36px; table rows comfortable for touch.

## Surfaces: Marketing vs Product

The single most useful distinction when applying this system:

| | Marketing (site) | Product (app) |
|---|---|---|
| Text ramp | Navy (`{colors.navy-800}`) | Slate (`{colors.slate-900}` → `{colors.slate-400}`) |
| Body size | `{typography.body}` 16px | `{typography.body-sm}` 14px |
| Headlines | DM Sans 500 + Fraunces italic | roman Fraunces page titles |
| Primary button | `{colors.navy-150}` muted | `{colors.navy-800}` solid (+ teal action) |
| Crosshair corners | Yes | No |
| Density | Generous, editorial | Compact, functional |

## Iteration Guide

1. Decide the surface first (marketing vs product) — it sets the text ramp, body size, and primary-button style.
2. Reference components by their `components:` token name.
3. Default corners to `{rounded.sharp}`; reach for `{rounded.nav}` only on the nav.
4. For headlines, write DM Sans 500 and mark the accent phrase as Fraunces italic.
5. Keep amber scarce; let teal carry action and navy carry brand.
6. Run `npx @google/design.md lint DESIGN.md` after edits.
7. Add new variants as separate component entries (e.g. `button-*`, `badge-*`).

## Known Gaps

- **Accessibility / contrast.** Several real brand pairs fall below WCAG AA (4.5:1): the `{components.button-action}` teal with white text (~2.6:1), the muted `{components.button-primary-marketing}`, the before/after comparison tints, `{colors.success}` on its tint (~4.5:1 borderline), and `{colors.slate-400}` eyebrows/labels. These are the brand's actual values — tune (darker teal, heavier label weight, larger sizes, or AAA-safe text colors) wherever AA compliance is required.
- **Product dark mode is extrapolated.** The Phase-1 Figma file ships the product in light only; the dark product tokens here are derived from the site's dark theme. Validate against a real dark-mode product design before treating them as canonical.
- **Icon set** is not specified — the product uses a line-icon family (placeholders used in review). Document the actual icon library when chosen.
- **Hover/focus states** for most components are partially documented (buttons, nav, crosshair animation). A full interaction-state pass (disabled, loading, error-validation on inputs) is pending.
- **Feature-card top rule** renders ~1px in the live CSS but reads thicker; documented at 3px to match design intent — confirm the exact weight.
- **Motion** (the crosshair hover animation, nav transitions ~400ms) is noted but not fully specified.
- The exact per-card accent assignment for the three marketing feature cards is representative (teal / slate / amber); confirm against final design.
