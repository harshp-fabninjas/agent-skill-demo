---
name: fabninjas-brand-design
description: >-
  Applies the official FabNinjas brand system — colours (#282643, #e99d75,
  #776482, #baa9b8, #f2e1ca), the Libre Franklin typeface, logo/favicon rules,
  and brand voice — to any content so it stays on-brand. Use when designing,
  generating, or reviewing FabNinjas material: "design a landing page", "make a
  social/LinkedIn/Instagram post", "create a banner", "make a slide deck",
  "build a FabNinjas email", "brand these visuals", "what are our brand
  colours/fonts", "match our brand", or producing any FabNinjas post, graphic,
  ad, or marketing copy.
---

# FabNinjas Brand Design

Keep every FabNinjas artifact — social posts, decks, landing pages, banners, emails,
docs — visually and verbally on-brand. This skill holds the concrete, approved rules
extracted from `FabNinjas_BrandGuidelines.pdf`. **All values below come from that source;
never invent or approximate colours, fonts, or logo treatments.** Items the source does
not define are flagged as recommendations.

## Brand in one line

FabNinjas builds unique, scalable, robust tech (web applications today) for a selective
clientele that brings the hard, "complicated" problems. Values: **creativity, enthusiasm,
humanity.** Voice: *expert builders who love hard problems — warm, sharp, quietly confident.*

## Colour tokens (exact — use verbatim)

| Token  | Hex       | RGB           | Role       | Primary use |
|--------|-----------|---------------|------------|-------------|
| ink    | `#282643` | 40, 38, 67    | primary    | Logo, headings, body text, dark sections (dominant colour) |
| orange | `#e99d75` | 233, 157, 117 | accent     | Highlights, CTA fills, illustration (the "stand out") |
| purple | `#776482` | 119, 100, 130 | secondary  | Dividers, underlines, secondary buttons (white text) |
| mauve  | `#baa9b8` | 186, 169, 184 | supporting | Soft backgrounds, borders, muted UI |
| cream  | `#f2e1ca` | 242, 225, 202 | neutral    | Warm background wash, cards (with ink text) |

**Contrast rules (verified):** ink-on-white ✅ and white-on-ink ✅ are the workhorses.
Buttons: orange fill + ink label, purple fill + white label, or ink fill + white label.
**Never** put ink text on purple (fails) or use orange/mauve/cream as text on white.
Full palette, ratios, and proportions → `references/colour-system.md`.

## Typography

- **Libre Franklin is the only typeface** — all headings and body. `font-family: "Libre Franklin", sans-serif;`
- **Never distort it** (no stretch/condense/skew/outline).
- **Tracking 0, leading auto** by default; build hierarchy with real weights (Black → Regular), not distortion.
- Libre Franklin is free on Google Fonts (SIL OFL); no font files ship with the brand. Weight scale, rules, and setup → `references/typography.md`.

## Logo

- Use the supplied art **as-is, one unit** — the *only* permitted change is its colour (ink / white / black).
- Default: `assets/logo/fabninjas-logo-navy.png` on light backgrounds; `fabninjas-logo-white.png` on dark.
- Tight spaces → the `fn` favicon (`assets/logo/favicon-*`).
- Never redraw, distort, recolour off-brand, add effects, or rearrange the lockup.
- All variants, background pairing, clear-space/min-size (recommended) → `references/logo-usage.md`.

## Voice & tone

Voice: *expert builders who love hard problems — warm, sharp, quietly confident*
(brand values: creativity, enthusiasm, humanity). Write in first-person plural, lead with
the client's outcome, and use concrete engineering language with a light touch of ninja wit.

- Avoid hollow hype ("world-class", "revolutionary", "synergy") — say something concrete instead.
- Don't claim offerings beyond FabNinjas' stated scope (web apps today, broader tech products over time).
- Example — ❌ "We leverage cutting-edge synergies to deliver world-class solutions." ✅ "We turn tricky ideas into scalable web products — and stick around as they grow."

This voice is derived from the About Us copy and stated values, not an explicit voice section in the source.

## Assets

```
palette.json                    machine-readable colour tokens (source of truth)
assets/logo/
  fabninjas-logo-navy.png       fabninjas-logo-white.png    fabninjas-logo-black.png
  favicon-fn-navy.png           favicon-fn-white.png        favicon-fn-black.png
  favicon-circle-navy.png       favicon-circle-white.png    favicon-circle-black.png
```
Reference by relative path (e.g. `assets/logo/fabninjas-logo-navy.png`). Logos are
4500×4500 transparent PNGs — this skill is the canonical home for the brand assets.

## Common mistakes

- Approximating hex values instead of using the exact five (they're in `palette.json`).
- Introducing off-brand colours (new blues/greens, pure `#000`, grays) or gradients.
- Low-contrast text: orange/mauve/cream on white, or ink on purple.
- Substituting another font for Libre Franklin, or stretching/letter-spacing type.
- Redrawing or distorting the logo; recolouring it outside ink/white/black.
- Navy logo on a dark background (or white logo on light) — pick the contrasting version.
- Using the full logo where it's too small to read — switch to the favicon.
- Hollow marketing hype, or claiming products beyond FabNinjas' stated scope.

## Reference index

- `references/colour-system.md` — full palette, RGB, contrast table, proportions, do/don't.
- `references/typography.md` — Libre Franklin rules, weight scale, where to get the font.
- `references/logo-usage.md` — every logo/favicon variant, background pairing, misuse, clear-space.

## Not defined in the source (flagged — don't present as official)

- **No font files** in the brand folder (Libre Franklin named only) — install from Google Fonts (SIL OFL).
- **No clear-space or minimum-size** values — recommendations given in `logo-usage.md`.
- **No type scale / weight spec** — recommended scale in `typography.md`.
- **No semantic colour roles or proportions** — inferred from swatch prominence/usage.
- **No explicit voice section** — the Voice & tone guidance above is derived from the About Us copy.
