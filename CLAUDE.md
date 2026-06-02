# RevenueBase Design System

This repo contains the RevenueBase design system: color tokens, typography, interactive review pages, brand assets, and HubSpot email modules for portal **8486714**.

## Repo layout

```
revenuebase-design-system/
├── DESIGN.md                          # Full design system (Google design.md / VoltAgent format)
├── CLAUDE.md                          # This file — project context for Claude Code
├── foundations.html                   # Color, type, spacing, texture — interactive (light/dark toggle)
├── marketing.html                     # Marketing components — interactive
├── product.html                       # Product components — interactive
├── assets/
│   ├── revenuebase-logo.svg           # Vector logo (web only — not email-safe)
│   ├── revenuebase-logo.png           # Logo on white bg (email header)
│   ├── revenuebase-logo-grey.png      # Logo on #f1f4f9 bg (email footer)
│   ├── bg-noise-light.webp            # 256px noise grain, light mode
│   ├── bg-noise-dark.webp             # 256px noise grain, dark mode
│   ├── grid-light.svg                 # 45px hairline grid, light
│   └── grid-dark.svg                  # 45px hairline grid, dark
├── bin/
│   └── push-module                    # Push a module to HubSpot (see below)
└── email/
    ├── revenuebase-marketing-email.html    # Coded HubSpot email template
    ├── feature-update-email.html           # Coded HubSpot email template
    ├── preview.html                        # Local preview
    ├── feature-update-preview.html         # Local preview
    └── modules/
        └── rb-*.module/                    # 16 HubSpot DnD email modules
            ├── meta.json
            ├── fields.json
            └── module.html
```

---

## Pushing modules to HubSpot

```bash
# Push one module
bin/push-module rb-hero

# Push all 16 modules
bin/push-module --all
```

The script reads `HUBSPOT_PAK` from the environment or from `.env` (gitignored). Copy `.env.example` to `.env` and add your key. The key needs `cms.source_code.write` and `files` scopes.

---

## Design system — key facts

### Two surfaces, two themes
- **Marketing** (revenuebase.ai): brand-saturated, DM Sans + Fraunces-italic headlines, 16px body, muted navy-150 primary button, crosshair corners on CTAs.
- **Product** (the app): functional, slate text ramp, DM Sans 14px body, solid navy-800 primary, teal action buttons. No crosshair corners in-product.
- Both surfaces ship **light and dark** themes. Neither uses pure `#fff` or `#000` — both are navy-tinted.

### Colors — commit these to memory

```
/* Navy (primary brand) */
navy-50:  #f1f4f9   ← light canvas / page background
navy-150: #c1cfe0   ← marketing primary button fill (quiet/muted)
navy-200: #b5c8e0   ← dark-mode secondary text; CTA banner button fill
navy-300: #89a5cc   ← borders, input borders
navy-800: #0f537e   ← primary brand color; marketing text; links
navy-850: #0a3652   ← dark surface
navy-900: #0e1a2e   ← dark canvas; CTA banner background

/* Amber/Gold (signature accent — logo mark ONLY) */
amber-100: #fff0cc  ← brand accent background (light)
amber-200: #ffe099  ← brand accent
amber-800: #704700  ← brand accent text

/* Teal (action accent) */
teal-500: #00b5b0   ← action color (light mode)
teal-400: #2dc9c4   ← action color (dark mode)
teal-600: #219f98   ← feature card top rule (teal variant)

/* Slate (neutral — product text ramp) */
slate-900: #13161d  ← product headings
slate-700: #2e323d  ← product body
slate-400: #868c9b  ← product muted / captions

/* Semantic */
success:  #2e7d32   ← active/free badges (bg: #e6f3e6)
danger:   #c62828   ← cancel, negative values (bg: #fae3e3)
warning:  #bf7c00   ← alert banners (bg: #fff8e6)
```

### Typography

| Family | Role | Weights |
|---|---|---|
| **DM Sans** | Headlines (500), all body text, UI, buttons | 400, 500, 600 |
| **Fraunces** | Italic accent words in marketing headlines; roman serif for product page titles (Data Catalog, Plan & Billing); stat figures | 400 italic / 600 roman |
| **JetBrains Mono** | Eyebrows, micro-labels (always uppercase + letter-spaced), code | 500 |

**The headline rule:** marketing headlines are DM Sans 500 with one phrase in Fraunces italic at ~1.07× size — e.g. `The trust layer` *`for B2B data.`*

**Google Fonts import — required in every module's `module.html`:**
```html
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600&family=Fraunces:ital,opsz,wght@1,9..144,400&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">
```

### Shape — 0px everywhere

Everything is square: buttons, inputs, cards, tags, panels. **One exception:** the floating nav bar at `8px`. No pills, no rounded cards, no softening.

### Texture

| Asset | Usage |
|---|---|
| `bg-noise-light/dark.webp` | 256px tile at exactly **4% opacity** over the canvas |
| `grid-light/dark.svg` | 45px hairline tile (0.5px stroke) on framed surfaces — not full pages |

### Logo assets

| File | Use | Hosted URL |
|---|---|---|
| `assets/revenuebase-logo.png` | Email header (white bg) | `https://8486714.fs1.hubspotusercontent-na1.net/hubfs/8486714/revenuebase/revenuebase-logo.png` |
| `assets/revenuebase-logo-grey.png` | Email footer (`#f1f4f9` bg) | `https://8486714.fs1.hubspotusercontent-na1.net/hubfs/8486714/revenuebase/revenuebase-logo-grey.png` |
| `assets/revenuebase-logo.svg` | Web pages only (not email-safe) | — |

Use the **grey logo in the footer** — it sits on `#f1f4f9` and has no white box. Use the **white logo in the header** — it sits on white.

---

## HubSpot email modules — complete inventory

All 16 modules live in `email/modules/` and are live on HubSpot portal 8486714. Search **"RB"** in the DnD email editor module list.

| Module directory | HubSpot label | Editable fields |
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
| `rb-checklist` | RB Checklist | `icon_style` (check/arrow/dot), `item1`–`item6` |
| `rb-logo-strip` | RB Logo Strip | `strip_eyebrow`, `logo1_src`–`logo4_src`, `logo_height`, `strip_bg` |
| `rb-divider` | RB Divider | `line_style` (solid/dashed/none), `line_color` (light/medium/dark), `spacing_top`, `spacing_bottom` |
| `rb-spacer` | RB Spacer | `spacer_height` (8/16/24/40/64) |
| `rb-footer` | RB Footer | `logo_src`, `logo_alt`, `logo_width`, `footer_tagline`, `unsubscribe_text`, `prefs_text` |

---

## Building a new module

### File structure
Each module is a directory `email/modules/rb-<name>.module/` with exactly three files:

**`meta.json`**
```json
{
  "label": "RB Module Name",
  "host_template_types": ["EMAIL"],
  "is_available_for_new_content": true,
  "smart_type": "NOT_SMART",
  "content_tags": []
}
```

**`fields.json`** — array of field objects. Field `type` values: `text`, `richtext`, `number`, `choice`.

**`module.html`** — always starts with the Google Fonts `<link>` tag, then HubL, then email-safe table HTML with inline CSS.

### Reserved field names — NEVER use these as `name` values
`body`, `title`, `name`, `label`, `content`, `type`, `id`, `key`, `class`, `style`

Use safe alternatives: `body_text`, `card_title`, `heading_text`, `content_text`, `item_text`, `module_style`, etc. HubSpot returns a hard `400` error if you use a reserved name.

### Padding standard
- Horizontal: `40px` on all sides
- Vertical: `24px` (standard) · `14px` (header) · `32px` (footer) · `40px` (CTA banner)

### URL fields in HubL
Never put `{% text %}` inside an `href="..."` — it renders as raw HTML and breaks the link. Use:
```html
{% text "button_url" label="Button URL", value="https://...", export_to_template_context=True %}
<a href="{{ widget_data.button_url.value }}">...</a>
```

### CAN-SPAM — never hardcode the address
HubSpot validates that email templates contain the `site_settings.company_*` tokens. Use:
```html
{{ site_settings.company_name }} · {{ site_settings.company_street_address_1 }},
{{ site_settings.company_city }}, {{ site_settings.company_state }} {{ site_settings.company_zip }}
```
Set the actual values at **Settings → Marketing → Email → Configuration**.

### Typical new-module workflow
1. Create `email/modules/rb-<name>.module/` with the three files
2. Prepend the Google Fonts `<link>` tag to `module.html`
3. Use safe field names
4. Run `bin/push-module rb-<name>` to deploy
5. Verify in a DnD email draft (search "RB" in module list)
6. Commit and push: `git add email/modules/rb-<name>.module && git commit -m "add rb-<name> module" && git push`

---

## Common HubSpot push errors

| Error | Cause | Fix |
|---|---|---|
| `field name cannot be 'body'` | Reserved field name | Rename to `body_text` |
| `Must contain site_settings.company_street_address_1` | Removed CAN-SPAM tokens | Restore `{{ site_settings.company_* }}` in footer |
| `Unable to process annotated template metadata` | Prose in the YAML annotation block | Move description outside the YAML comment |
| `403 MISSING_SCOPES — requires 'content'` | PAK lacks marketing email scope (unfixable on PAK) | Use the HubSpot UI to create/send emails; PAK only covers CMS + files |

---

## Do's and Don'ts

**Do**
- Start every `module.html` with the Google Fonts `<link>` tag
- Use `40px` horizontal padding in all module cells
- Use `0px` border-radius on everything (nav is the one 8px exception)
- Keep amber reserved for the logo mark and brand accent moments only
- Use the grey logo (`revenuebase-logo-grey.png`) in the footer
- Test in a HubSpot DnD email draft before shipping

**Don't**
- Don't use reserved field names (`body`, `title`, `name`, `label`…)
- Don't put `{% text %}` inside an `href` attribute — it breaks links
- Don't hardcode the company address in email templates
- Don't use `border-radius` on buttons, cards, or inputs — the system is square
- Don't put crosshair corner marks in product-surface elements (marketing only)
- Don't use amber as a button fill or large background
- Don't use SVG in email (Outlook/Gmail don't render it) — use hosted PNG
