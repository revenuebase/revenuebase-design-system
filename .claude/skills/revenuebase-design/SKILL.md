---
name: revenuebase-design
description: RevenueBase design system — build, update, and push HubSpot email modules; answer design questions; enforce brand tokens. (RevenueBase)
triggers:
  - revenuebase design system
  - build a module
  - push a module
  - new email module
  - update module
  - design token
  - brand colors
  - email template
allowed-tools:
  - Bash
  - Read
  - Write
  - Edit
  - AskUserQuestion
---

## When to invoke this skill

Use when working with the RevenueBase design system: creating or updating HubSpot email modules, answering questions about brand tokens (colors, typography, spacing), building email templates, or pushing assets to HubSpot portal 8486714.

## Preamble

```bash
_REPO=$(git rev-parse --show-toplevel 2>/dev/null || echo "$HOME/Documents/GitHub/revenuebase-design-system")
echo "REPO: $_REPO"
echo "MODULES: $_REPO/email/modules"
ls "$_REPO/email/modules" 2>/dev/null | sed 's/\.module//' | tr '\n' ' '
echo ""
# Check for PAK
if [ -n "${HUBSPOT_PAK:-}" ]; then
  echo "PAK: env var set"
elif grep -q "^HUBSPOT_PAK=" "$_REPO/.env" 2>/dev/null; then
  echo "PAK: .env file found"
else
  echo "PAK: NOT CONFIGURED — add HUBSPOT_PAK=<key> to $_REPO/.env before pushing"
fi
```

---

## Design System Overview

RevenueBase is a B2B data-infrastructure brand. The design system spans **two surfaces** (marketing site + product app) and **two themes** (light + dark, both navy-tinted — never pure `#fff`/`#000`). The system reads as infrastructure: square, precise, technical.

---

## Color Tokens

### Palette ramps

| Scale | Core value | Role |
|---|---|---|
| **Navy** | `#0f537e` (navy-800) | Primary brand — marketing text, product interactive, links |
| **Amber/Gold** | `#ffe099` (amber-200) | Signature accent — logo mark and brand moments ONLY |
| **Teal** | `#00b5b0` (teal-500) | Action accent — progress, checks, product action buttons |
| **Slate** | `#2e323d` (slate-700) | Neutral — product text hierarchy and dividers |

### Key values (commit these to memory)

```
navy-50:   #f1f4f9   ← light canvas
navy-100:  #dde6f1
navy-150:  #c1cfe0   ← marketing primary button fill
navy-200:  #b5c8e0   ← dark-mode text-secondary; CTA button fill
navy-300:  #89a5cc   ← borders, input borders
navy-800:  #0f537e   ← primary brand, marketing text, nav link color
navy-850:  #0a3652   ← dark surface
navy-900:  #0e1a2e   ← dark canvas, CTA banner background

amber-200: #ffe099   ← brand accent background
amber-800: #704700   ← brand accent text

teal-500:  #00b5b0   ← action (light mode)
teal-400:  #2dc9c4   ← action (dark mode)
teal-600:  #219f98   ← feature card top rule (teal variant)

slate-900: #13161d   ← product heading text
slate-700: #2e323d   ← product body text
slate-400: #868c9b   ← product muted / captions

success:   #2e7d32   ← active/free badges
danger:    #c62828   ← cancel, sign out, negative values
warning:   #bf7c00   ← alert banners
```

### Light/Dark theme mapping

| Role | Light | Dark |
|---|---|---|
| canvas | `#f1f4f9` navy-50 | `#0e1a2e` navy-900 |
| surface | `#ffffff` | `#0a3652` navy-850 |
| action | `#00b5b0` teal-500 | `#2dc9c4` teal-400 |
| brand accent bg | `#fff0cc` amber-100 | `#4d3000` amber-900 |
| brand accent text | `#704700` amber-800 | `#fff8e6` amber-50 |

---

## Typography

Three families — all open-source Google Fonts:

| Family | Role | Weights |
|---|---|---|
| **DM Sans** | Headlines (500), body, UI, buttons | 400, 500, 600 |
| **Fraunces** | Italic accent words in marketing headlines; roman serif for product page titles; stat figures | 400 italic |
| **JetBrains Mono** | Eyebrows, labels (always uppercase), code | 500 |

### The headline rule
Marketing headlines are **DM Sans 500** with one phrase swapped to **Fraunces italic** at 1.07× size:
> `The trust layer` *`for B2B data.`*

Product page titles (Data Catalog, Plan & Billing) use roman **Fraunces** — not DM Sans.

### Google Fonts import (required in every module)
```html
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600&family=Fraunces:ital,opsz,wght@1,9..144,400&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">
```
Always prepend this to every `module.html`. Without it, fonts fall back to Arial/Georgia/Courier.

---

## Shape

**Everything is 0px.** Buttons, inputs, cards, tags, panels — all square.  
**One exception:** the floating nav bar at 8px.

### Crosshair corners (marketing only)
Marketing CTAs and framed panels have `c-crosshair` corner marks — small `+` marks just outside each corner. In-product chrome has NO crosshairs.

```html
<!-- Add to marketing buttons: -->
<i class="cm cm-tl"></i><i class="cm cm-tr"></i>
<i class="cm cm-bl"></i><i class="cm cm-br"></i>
```

---

## Texture

| Asset | Path | Usage |
|---|---|---|
| Noise grain (light) | `assets/bg-noise-light.webp` | 256px tile at **4% opacity** over canvas |
| Noise grain (dark) | `assets/bg-noise-dark.webp` | 256px tile at **4% opacity** over canvas |
| Hairline grid (light) | `assets/grid-light.svg` | 45px tile, 0.5px stroke, slate-200 |
| Hairline grid (dark) | `assets/grid-dark.svg` | 45px tile, 0.5px stroke, navy-850 |

---

## Logo Assets

| Asset | Local path | Hosted URL |
|---|---|---|
| Logo (white bg) | `assets/revenuebase-logo.png` | `https://8486714.fs1.hubspotusercontent-na1.net/hubfs/8486714/revenuebase/revenuebase-logo.png` |
| Logo (grey bg `#f1f4f9`) | `assets/revenuebase-logo-grey.png` | `https://8486714.fs1.hubspotusercontent-na1.net/hubfs/8486714/revenuebase/revenuebase-logo-grey.png` |
| Logo SVG (web only) | `assets/revenuebase-logo.svg` | — (SVG not email-safe) |

Use **grey logo** in the footer (sits on `#f1f4f9` background).  
Use **white logo** in the header (sits on white).  
Use **SVG** only in the web review pages (foundations.html, marketing.html, product.html).

---

## Buttons (marketing surface)

| Variant | Background | Text | Border | Radius |
|---|---|---|---|---|
| Primary | `#c1cfe0` navy-150 (muted) | `#0f537e` navy-800 | `#89a5cc` navy-300 | 0px |
| Secondary | transparent | `#0f537e` navy-800 | `#89a5cc` navy-300 | 0px |
| Nav | `#c1cfe0` navy-150 | `#0f537e` navy-800 | none | 8px |

The primary is deliberately **quiet** (muted fill, not saturated). Teal fills are product-only.

---

## HubSpot Module Structure

Each module lives in `email/modules/<name>.module/` with three files:

### `meta.json`
```json
{
  "label": "RB Module Name",
  "host_template_types": ["EMAIL"],
  "is_available_for_new_content": true,
  "smart_type": "NOT_SMART",
  "content_tags": []
}
```

### `fields.json`
Array of field objects. **RESERVED NAMES — never use these as `name` values:**
- `body`, `title`, `name`, `label`, `content`, `type`, `id`, `key`, `class`, `style`

Use safe alternatives: `body_text`, `card_title`, `heading_text`, `content_text`, `item_text`, etc.

```json
[
  { "name": "heading_text", "label": "Heading", "type": "text", "default": "..." },
  { "name": "body_text", "label": "Body", "type": "richtext", "default": "<p>...</p>" },
  {
    "name": "style_choice",
    "label": "Style",
    "type": "choice",
    "display": "select",
    "choices": [["option1", "Label 1"], ["option2", "Label 2"]],
    "default": "option1"
  }
]
```

### `module.html`
Always starts with the Google Fonts `<link>` tag, then HubL template logic, then email-safe table HTML with inline CSS.

```html
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600&family=Fraunces:ital,opsz,wght@1,9..144,400&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">
{% if module.style_choice == "navy" %}{% set bg = "#dde6f1" %}{% endif %}
<table role="presentation" width="100%" cellpadding="0" cellspacing="0" border="0"><tr>
  <td style="padding:24px 40px; background:{{ bg }}; font-family:'DM Sans',Arial,Helvetica,sans-serif;">
    {{ module.body_text }}
  </td>
</tr></table>
```

### Padding standard
All modules use `40px` horizontal padding and `24px` vertical (except header `14px` vertical, footer `32px` vertical, CTA `40px` vertical, stat strip `18px` vertical).

---

## Existing Modules (16)

| Module | Label in HubSpot | Key fields |
|---|---|---|
| `rb-header` | RB Header | `logo_src`, `logo_alt`, `logo_width`, `tagline_text`, `tagline_url` |
| `rb-hero` | RB Hero | `eyebrow`, `headline`, `headline_accent`, `body_text` |
| `rb-section-heading` | RB Section Heading | `eyebrow`, `heading_text` |
| `rb-text` | RB Text | `content_text`, `text_size` (sm/md/lg), `text_align` |
| `rb-image` | RB Image | `img_src`, `img_alt`, `img_link`, `img_width`, `img_align`, `caption_text` |
| `rb-feature-card` | RB Feature Card | `accent` (teal/navy/amber), `eyebrow`, `card_title`, `body_text` |
| `rb-button` | RB Button | `button_text`, `button_url`, `style` (navy/teal/outline), `align` |
| `rb-cta` | RB CTA Banner | `eyebrow`, `headline_accent`, `headline`, `button_text`, `button_url` |
| `rb-stat-strip` | RB Stat Strip | `text` |
| `rb-stat-figures` | RB Stat Figures | `stat1_figure`, `stat1_caption`, `stat2_*`, `stat3_*` |
| `rb-quote` | RB Quote | `quote_text`, `person_name`, `person_role` |
| `rb-checklist` | RB Checklist | `icon_style` (check/arrow/dot), `item1`…`item6` |
| `rb-logo-strip` | RB Logo Strip | `strip_eyebrow`, `logo1_src`…`logo4_src`, `logo_height`, `strip_bg` |
| `rb-divider` | RB Divider | `line_style` (solid/dashed/none), `line_color` (light/medium/dark), `spacing_top`, `spacing_bottom` |
| `rb-spacer` | RB Spacer | `spacer_height` (8/16/24/40/64) |
| `rb-footer` | RB Footer | `logo_src`, `logo_alt`, `logo_width`, `footer_tagline`, `unsubscribe_text`, `prefs_text` |

---

## Pushing Modules to HubSpot

### Setup (one-time)
Add your HubSpot Personal Access Key to `.env` (already gitignored):
```
HUBSPOT_PAK=your-key-here
```
The key needs `cms.source_code.write` and `files` scopes.

### Push a single module
```bash
.claude/skills/revenuebase-design/bin/push-module rb-hero
```

### Push all modules
```bash
.claude/skills/revenuebase-design/bin/push-module --all
```

### Push via API directly (if needed)
```bash
# 1. Get token
TOKEN=$(curl -s -X POST "https://api.hubapi.com/localdevauth/v1/auth/refresh" \
  -H "Content-Type: application/json" \
  -d "{\"encodedOAuthRefreshToken\":\"$HUBSPOT_PAK\"}" | \
  python3 -c "import sys,json; print(json.load(sys.stdin)['oauthAccessToken'])")

# 2. Push a file
curl -X PUT "https://api.hubapi.com/cms/v3/source-code/published/content/revenuebase/modules/rb-hero.module/module.html" \
  -H "Authorization: Bearer $TOKEN" \
  -F "file=@email/modules/rb-hero.module/module.html"
```

### Common errors
| Error | Cause | Fix |
|---|---|---|
| `field name cannot be 'body'` | Reserved field name | Rename to `body_text` |
| `Must contain site_settings.company_street_address_1` | CAN-SPAM — removed address tokens | Restore `{{ site_settings.company_* }}` tokens |
| `Unable to process annotated template metadata` | Prose in YAML annotation | Move description into a separate HTML comment block |
| `403 MISSING_SCOPES` | Key lacks `content` scope | PAK only supports CMS/files; marketing email API needs Private App |

---

## Do's and Don'ts

### Do
- Start every `module.html` with the Google Fonts `<link>` tag
- Use `40px` horizontal, `24px` vertical padding in module cells
- Use `0px` border-radius on everything except the nav (8px)
- Keep amber reserved for logo moments and brand accent only
- Use `body_text` not `body`; `card_title` not `title`; `heading_text` not `title`
- Use `export_to_template_context=True` on URL text fields and print with `{{ widget_data.*.value }}`
- Use the grey logo in the footer (it sits on `#f1f4f9`)
- Test the module in a DnD email draft before announcing it's done

### Don't
- Don't use SVG in email (no client support) — use hosted PNG
- Don't use reserved field names: `body`, `title`, `name`, `label`, `content`, `id`, `key`
- Don't hardcode the company address — use `{{ site_settings.company_* }}` tokens
- Don't add crosshair corners to product-surface elements
- Don't use `border-radius` on buttons, cards, inputs — everything is square
- Don't put amber on a button or large fill
- Don't use `{% text "url" %}` inside an `href=""` attribute — it breaks the link

---

## File Layout

```
revenuebase-design-system/
├── DESIGN.md                          # Full design system (Google design.md format)
├── foundations.html                   # Color, type, spacing, themes — interactive
├── marketing.html                     # Marketing components — interactive
├── product.html                       # Product components — interactive
├── assets/
│   ├── revenuebase-logo.svg           # Vector logo (web only)
│   ├── revenuebase-logo.png           # Logo on white (email header)
│   ├── revenuebase-logo-grey.png      # Logo on #f1f4f9 (email footer)
│   ├── bg-noise-light.webp            # Noise grain, light mode
│   ├── bg-noise-dark.webp             # Noise grain, dark mode
│   ├── grid-light.svg                 # 45px hairline grid, light
│   └── grid-dark.svg                  # 45px hairline grid, dark
└── email/
    ├── revenuebase-marketing-email.html    # HubSpot coded template
    ├── feature-update-email.html           # HubSpot coded template
    ├── preview.html                        # Local preview (marketing)
    ├── feature-update-preview.html         # Local preview (feature update)
    └── modules/
        └── rb-*.module/                    # 16 HubSpot DnD email modules
            ├── meta.json
            ├── fields.json
            └── module.html
```

---

## Workflow: Adding a New Module

1. Create `email/modules/rb-<name>.module/` with `meta.json`, `fields.json`, `module.html`
2. Start `module.html` with the Google Fonts `<link>` tag
3. Use safe field names (not reserved)
4. Test padding: `40px` horizontal, appropriate vertical
5. Run push: `.claude/skills/revenuebase-design/bin/push-module rb-<name>`
6. Verify in HubSpot DnD email editor (search "RB" in module list)
7. Commit: `git add email/modules/rb-<name>.module && git commit -m "add rb-<name> module"`
8. Push: `git push`
