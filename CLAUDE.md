# RevenueBase Design System

Use this file as the authoritative brand and design reference for any RevenueBase creative output — slides, banners, images, email, app screens, documents, social graphics, ads, or anything else that needs to look like RevenueBase. When designing anything, check here first and apply these tokens consistently regardless of the medium.

---

## Brand identity

RevenueBase is a B2B data-infrastructure company. The brand reads as **infrastructure: square, precise, technical, and quietly confident**. It is not loud or flashy. It earns trust through restraint — muted primary buttons, hairline borders, blueprint corner-marks — not through saturated colors or decorative elements.

**Voice:** Direct. Data-first. No fluff. Confident without being arrogant.

**Visual personality:**
- Square corners everywhere — the squareness is intentional and should never be softened
- A navy-tinted palette (no pure black or white anywhere)
- Amber/gold reserved exclusively for the logo mark — never used as a button or fill
- Fraunces-italic as an editorial accent inside headlines, not a display typeface
- Blueprint details: crosshair corner marks, hairline grids, mono eyebrows in uppercase

---

## Logo

| File | URL | Use |
|---|---|---|
| Logo (SVG) | `https://revenuebase.github.io/revenuebase-design-system/assets/revenuebase-logo.svg` | Web, presentations, large-format digital |
| Logo (white bg PNG) | `https://revenuebase.github.io/revenuebase-design-system/assets/revenuebase-logo.png` | White backgrounds (email header, light slides) |
| Logo (grey bg PNG) | `https://revenuebase.github.io/revenuebase-design-system/assets/revenuebase-logo-grey.png` | `#f1f4f9` backgrounds (email footer, tinted panels) |

The logo mark is a gradient chevron (orange `#ff7708` → amber `#ffaa00`) + wordmark (**Revenue**Base — bold + regular weight). Never use a glyph or approximation.

**Clear space:** at least the height of the mark on all sides.  
**Minimum size:** 80px wide digital, 20mm print.  
**Don't:** recolor, stretch, add a drop shadow, or place on a busy background.

---

## Color

### Palette — four ramps

All colors are navy-tinted. Neither light nor dark mode uses pure `#ffffff` or `#000000`.

**Navy** (primary brand)
```
navy-50:   #f1f4f9   ← light canvas / page background
navy-100:  #dde6f1
navy-150:  #c1cfe0   ← marketing primary button (muted fill)
navy-200:  #b5c8e0   ← dark-mode text-secondary; inverse button fill
navy-300:  #89a5cc   ← borders, dividers, input strokes
navy-400:  #5e82b8
navy-500:  #43649f
navy-600:  #2e5a82
navy-700:  #1a4a6e
navy-800:  #0f537e   ← primary brand; marketing headings; links
navy-850:  #0a3652   ← dark surface
navy-900:  #0e1a2e   ← dark canvas; CTA banner background
navy-950:  #091220
```

**Amber / Gold** (signature accent — logo and brand moments only)
```
amber-50:  #fff8e6
amber-100: #fff0cc
amber-200: #ffe099   ← brand accent highlight
amber-300: #ffce66
amber-600: #bf7c00
amber-700: #946000
amber-800: #704700   ← brand accent text
amber-900: #4d3000
```
⚠️ Amber never fills a button, section background, or large surface. It is used sparingly for accent chips, badges, eyebrows, and brand moments.

**Teal** (action accent)
```
teal-50:  #ecfcfb
teal-100: #cff5f4
teal-400: #2dc9c4   ← action (dark mode)
teal-500: #00b5b0   ← action (light mode) — progress bars, checks, primary product buttons
teal-600: #219f98
teal-700: #107069
```

**Slate** (neutral — product text and dividers)
```
slate-50:  #f7f7f9
slate-100: #ecedf0
slate-200: #d2d5dc   ← light dividers
slate-300: #adb2bd
slate-400: #868c9b   ← muted / captions
slate-500: #626879
slate-700: #2e323d   ← product body text
slate-900: #13161d   ← product heading text
```

**Semantic**
```
success:     #2e7d32   on background #e6f3e6
danger:      #c62828   on background #fae3e3
warning:     #bf7c00   on background #fff8e6
```

### Light vs dark themes

| Role | Light | Dark |
|---|---|---|
| Canvas / background | `#f1f4f9` navy-50 | `#0e1a2e` navy-900 |
| Surface / card | `#ffffff` | `#0a3652` navy-850 |
| Primary heading text | `#0f537e` navy-800 (marketing) / `#13161d` slate-900 (product) | `#f1f4f9` navy-50 |
| Body text | `#2e323d` slate-700 | `#b5c8e0` navy-200 |
| Muted text | `#868c9b` slate-400 | `#89a5cc` navy-300 |
| Border | `#d2d5dc` slate-200 (product) / `#b5c8e0` navy-200 (marketing) | `#1a4a6e` navy-700 |
| Action | `#00b5b0` teal-500 | `#2dc9c4` teal-400 |
| Brand accent | amber-100 bg / amber-800 text | amber-900 bg / amber-50 text |

---

## Typography

Three families, all Google Fonts (open source):

| Family | Role | Weights |
|---|---|---|
| **DM Sans** | Headlines, body, UI labels, buttons, navigation | 400, 500, 600, 700 |
| **Fraunces** | Italic accent words within marketing headlines; roman serif for product page titles; large stat figures | 400 italic, 600 roman |
| **JetBrains Mono** | Eyebrows, micro-labels (always uppercase + letter-spaced), code, API references | 400, 500 |

### Type scale

| Role | Family | Size | Weight | Notes |
|---|---|---|---|---|
| Display / hero | DM Sans | 54–72px | 500 | With Fraunces-italic accent phrase |
| H1 | DM Sans | 46px | 500 | |
| H2 | DM Sans | 40px | 500 | |
| H3 | DM Sans | 30px | 500 | |
| Product page title | Fraunces | 26px | 600 | Roman, not italic |
| Card title | DM Sans | 19px | 600 | |
| Body large | DM Sans | 20px | 400 | Lead paragraphs |
| Body | DM Sans | 16px | 400 | Marketing default |
| Body small | DM Sans | 14px | 400 | Product UI default |
| Eyebrow | JetBrains Mono | 12–13px | 500 | UPPERCASE, +0.8px tracking |
| Label | JetBrains Mono | 11px | 500 | UPPERCASE, +1px tracking |
| Stat figure | Fraunces italic | 42–72px | 400 | For "1B+", "390M+", etc. |

### The headline rule
Marketing headlines are **DM Sans 500** with one phrase in **Fraunces italic** at approximately 1.07× the DM Sans size:
> The trust layer *for B2B data.*
> *We help* customers achieve measurable results.

Product page titles (e.g. "Data Catalog", "Plan & Billing") use roman **Fraunces** — not DM Sans, not italic.

### Letter spacing
Display: −0.03em · H1: −0.02em · Body: 0 · Eyebrow/label: +0.06–0.1em

---

## Shape

**Everything is 0px border-radius.** This is intentional and non-negotiable. Buttons, cards, inputs, tags, panels, images, slides — all square.

**One exception:** the floating navigation bar uses 8px.

Never soften the system with rounded corners. The squareness is the brand's infrastructure signal.

### Crosshair corner marks
A signature motif on marketing surfaces: small `+` registration marks just outside the corners of buttons and framed panels. Used on the website and marketing emails. **Not used in the product app or in documents/slides.**

---

## Spacing

4px base grid.

```
4px   · xxs
8px   · xs
12px  · sm
16px  · md
24px  · lg
32px  · xl
48px  · xxl
64px  · xxxl
80px  · section-sm
112px · section
160px · section-lg
```

---

## Texture

Two background textures — both lifted from the live site, both theme-aware:

| Asset | URL | How to use |
|---|---|---|
| Noise grain (light) | `https://revenuebase.github.io/revenuebase-design-system/assets/bg-noise-light.webp` | 256px tile at **4% opacity** over canvas |
| Noise grain (dark) | `https://revenuebase.github.io/revenuebase-design-system/assets/bg-noise-dark.webp` | 256px tile at **4% opacity** over canvas |
| Grid (light) | `https://revenuebase.github.io/revenuebase-design-system/assets/grid-light.svg` | 45px hairline tile (0.5px stroke) on framed panels |
| Grid (dark) | `https://revenuebase.github.io/revenuebase-design-system/assets/grid-dark.svg` | 45px hairline tile (0.5px stroke) on framed panels |

---

## Applying the system by medium

### Presentations (PowerPoint / Google Slides / Keynote)
- **Slide background:** `#f1f4f9` (light) or `#0e1a2e` (dark)
- **Headline:** DM Sans 500, navy-800, with one phrase in Fraunces italic where appropriate
- **Body:** DM Sans 400 16–18px, slate-700 (light) / navy-200 (dark)
- **Accent:** amber chip or teal rule — never amber as a section fill
- **Layout:** align to an 8-column grid with 40px margins. Keep it sparse.
- **Borders / dividers:** 1px slate-200 (light) or navy-700 (dark)
- **Images:** square crop, no rounded corners, thin navy-200 border if framed
- **Logo:** top-left, SVG or high-res PNG, white or grey version depending on bg
- **Do not:** use the built-in theme colors, rounded shapes, or drop shadows

### Banners / Display ads / Social graphics
- Same palette and type — navy headlines, DM Sans 500, Fraunces-italic accent
- Background: navy-50 (light) or navy-900 (dark) with optional noise texture at 4%
- CTA button: `#c1cfe0` fill, `#0f537e` text, 0px radius, crosshair corners
- For dark banners: amber eyebrow label, navy-50 headline
- Keep text minimal — the data does the talking
- Logo: always include, use the right variant for the background

### Images / Illustrations
- Stay within the navy/amber/teal/slate palette
- Use teal for highlights and active states
- Amber appears only as a small accent, never as a dominant color
- Illustrations and diagrams should feel technical and clean — no gradients, no drop shadows, sharp edges

### Documents (Word / PDF / reports)
- **Page background:** white `#ffffff` or `#f1f4f9`
- **Heading 1:** DM Sans 600, 28–32px, navy-800
- **Heading 2:** DM Sans 600, 20–24px, navy-800
- **Body:** DM Sans 400, 11–12pt, slate-700
- **Captions / labels:** JetBrains Mono 500, 9–10pt, uppercase, slate-400
- **Callout boxes:** navy-50 bg, navy-300 left border, 16px padding
- **Tables:** slate-100 header bg, hairline slate-200 borders
- **Logo:** top of cover page and header/footer

### Email (HubSpot DnD modules)
16 branded modules are live on HubSpot portal 8486714. Search **"RB"** in the module list. Full module specs and push workflow are in the sections below.

### Product / App UI
- Text ramp: slate-900 headings, slate-700 body, slate-400 muted
- Primary button: solid navy-800, white text
- Action button: teal-500, white text
- Page titles: Fraunces roman (not DM Sans)
- No crosshair corners in-product

---

## Design principles

1. **Square by default.** Never round corners except the nav (8px). Softening the system breaks the infrastructure signal.
2. **Amber is scarce.** It exists only in the logo and as small accent moments. It never fills a button or a section.
3. **Teal carries action.** Progress, checks, primary product buttons, and in-product CTAs use teal.
4. **The headline is DM Sans with a Fraunces-italic guest.** Never set a full headline in Fraunces.
5. **Both modes are navy-tinted.** Never use pure `#fff` or `#000` as a background.
6. **Texture is whisper-quiet.** The noise grain runs at 4% — it should be felt, not seen.
7. **No drop shadows.** Depth comes from surface tints and hairline borders.
8. **Crosshairs are marketing-only.** Not in the product, not in documents, not in slides.

---

## Assets in this repo

All assets are hosted at `https://revenuebase.github.io/revenuebase-design-system/assets/` — no repo clone needed.

| Asset | Hosted URL |
|---|---|
| Logo SVG | `https://revenuebase.github.io/revenuebase-design-system/assets/revenuebase-logo.svg` |
| Logo PNG (white bg) | `https://revenuebase.github.io/revenuebase-design-system/assets/revenuebase-logo.png` |
| Logo PNG (grey bg) | `https://revenuebase.github.io/revenuebase-design-system/assets/revenuebase-logo-grey.png` |
| Noise grain (light) | `https://revenuebase.github.io/revenuebase-design-system/assets/bg-noise-light.webp` |
| Noise grain (dark) | `https://revenuebase.github.io/revenuebase-design-system/assets/bg-noise-dark.webp` |
| Grid tile (light) | `https://revenuebase.github.io/revenuebase-design-system/assets/grid-light.svg` |
| Grid tile (dark) | `https://revenuebase.github.io/revenuebase-design-system/assets/grid-dark.svg` |

---

## HubSpot email modules

### Pushing modules to HubSpot
```bash
bin/push-module rb-hero      # push one module
bin/push-module --all        # push all 16
```
Requires `HUBSPOT_PAK` in environment or `.env`. Copy `.env.example` → `.env`.

### Module inventory (16 modules, portal 8486714)

| Module | Label | Key fields |
|---|---|---|
| `rb-header` | RB Header | `logo_src`, `tagline_text`, `tagline_url` |
| `rb-hero` | RB Hero | `eyebrow`, `headline`, `headline_accent`, `body_text` |
| `rb-section-heading` | RB Section Heading | `eyebrow`, `heading_text` |
| `rb-text` | RB Text | `content_text`, `text_size`, `text_align` |
| `rb-image` | RB Image | `img_src`, `img_alt`, `img_link`, `img_width`, `img_align`, `caption_text` |
| `rb-feature-card` | RB Feature Card | `accent` (teal/navy/amber), `eyebrow`, `card_title`, `body_text` |
| `rb-button` | RB Button | `button_text`, `button_url`, `style` (navy/teal/outline), `align` |
| `rb-cta` | RB CTA Banner | `eyebrow`, `headline_accent`, `headline`, `button_text`, `button_url` |
| `rb-stat-strip` | RB Stat Strip | `text` |
| `rb-stat-figures` | RB Stat Figures | `stat1_figure`, `stat1_caption`, `stat2_*`, `stat3_*` |
| `rb-quote` | RB Quote | `quote_text`, `person_name`, `person_role` |
| `rb-checklist` | RB Checklist | `icon_style` (check/arrow/dot), `item1`–`item6` |
| `rb-logo-strip` | RB Logo Strip | `strip_eyebrow`, `logo1_src`–`logo4_src`, `logo_height`, `strip_bg` |
| `rb-divider` | RB Divider | `line_style`, `line_color`, `spacing_top`, `spacing_bottom` |
| `rb-spacer` | RB Spacer | `spacer_height` (8/16/24/40/64) |
| `rb-footer` | RB Footer | `logo_src`, `footer_tagline`, `unsubscribe_text`, `prefs_text` |

### Module build rules
- Every `module.html` must start with the Google Fonts `<link>` tag
- **Never use reserved field names:** `body`, `title`, `name`, `label`, `content`, `type`, `id`, `key` — use `body_text`, `card_title`, `heading_text` etc. instead
- Never put `{% text %}` inside an `href` attribute — breaks the link. Use `export_to_template_context=True` and print with `{{ widget_data.*.value }}`
- Never hardcode the company address — use `{{ site_settings.company_* }}` tokens (CAN-SPAM requirement)

### Hosted logo URLs (for use in module defaults)
```
White bg:  https://8486714.fs1.hubspotusercontent-na1.net/hubfs/8486714/revenuebase/revenuebase-logo.png
Grey bg:   https://8486714.fs1.hubspotusercontent-na1.net/hubfs/8486714/revenuebase/revenuebase-logo-grey.png
```
