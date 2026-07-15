# FabNinjas Colour System

**Source:** `FabNinjas_BrandGuidelines.pdf`, page 3 — *"Colours That Help Us Stand Out."*
Guiding line from the source: *"Combination of purples and orange to depict creativity, enthusiasm and humanity."*

The five hex values below are **authoritative** (verbatim from the guidelines). The
**roles** (primary/secondary/etc.) are derived from swatch prominence in the source
artwork and how the document itself uses the colours — the PDF does **not** label roles.
See "Not defined in source" at the bottom.

## Approved palette (exact values — never approximate)

| Token  | Hex       | RGB           | Role       | Use it for |
|--------|-----------|---------------|------------|------------|
| ink    | `#282643` | 40, 38, 67    | primary    | Logo, headings, body text, dark backgrounds. Largest swatch = dominant colour. |
| orange | `#e99d75` | 233, 157, 117 | accent     | The stand-out accent. Fills, highlights, CTA backgrounds, illustration. |
| purple | `#776482` | 119, 100, 130 | secondary  | Dividers, heading underlines, secondary button fills (with white text). |
| mauve  | `#baa9b8` | 186, 169, 184 | supporting | Soft section backgrounds, borders, muted UI, chart series. |
| cream  | `#f2e1ca` | 242, 225, 202 | neutral    | Warm page/background wash, cards, callouts. Pair with `ink` text. |

Swatch prominence in the source (largest → smallest): **ink → orange ≈ purple ≈ mauve → cream.**
`ink` dominates; treat it as the backbone and let orange/purple do the "standing out."

## Contrast — verified WCAG ratios (use these, don't guess)

Body text needs ≥ 4.5:1; large/bold text (≥ 24px, or ≥ 19px bold) needs ≥ 3:1.

| Foreground | Background | Ratio | Verdict |
|------------|------------|-------|---------|
| ink `#282643`  | white       | **14.5** | Pass — default text pairing |
| ink `#282643`  | cream `#f2e1ca` | **11.3** | Pass — warm alt background |
| ink `#282643`  | mauve `#baa9b8` | **6.5**  | Pass |
| ink `#282643`  | orange `#e99d75`| **6.6**  | Pass — ink label on an orange button |
| white          | ink `#282643`   | **14.5** | Pass — reversed / dark sections |
| white          | purple `#776482`| **5.3**  | Pass — white label on a purple button |
| purple `#776482` | white     | **5.3**  | Pass — purple usable as text on white |
| ink `#282643`  | purple `#776482`| **2.7**  | **FAIL — never put ink text on purple** |
| orange `#e99d75` | white     | **2.2**  | **FAIL — orange is a fill, not text on white** |
| cream on white / mauve on white | — | ≤ 2.2 | Decorative only, never text |

Rules that fall out of the numbers:
- **Default text:** ink on white or ink on cream.
- **Reversed text:** white on ink. On purple, only white text (never ink).
- **Buttons:** orange fill + ink label, OR purple fill + white label, OR ink fill + white label.
- **Never** set orange, mauve or cream as text colour on a light background.

## Suggested proportion (recommendation — not in source)

A workable default when the guidelines give no ratio: ~60% neutral ground
(white / cream), ~25% ink structure, ~15% split between orange and purple accents,
with mauve as an occasional tint. Adjust per piece; keep orange as the spark, not the field.

## Do / Don't

- **Do** use the exact hex values (they're in `palette.json`); never eyeball or approximate.
- **Do** lead with ink; use orange sparingly so it keeps its "stand out" power.
- **Don't** introduce colours outside this list (no new blues, greens, pure black `#000`, or grays).
- **Don't** recolour the logo to anything other than ink / white / black (see `logo-usage.md`).
- **Don't** place low-contrast text (orange/mauve/cream on white, ink on purple).

## Not defined in source (flagged)

- No semantic role labels (primary/secondary/CTA) — roles here are inferred from prominence and usage.
- No fixed usage proportions — the 60/25/15 split above is a recommendation.
- No tint/shade ramp — if you need lighter/darker steps, derive them and validate contrast, but prefer the five approved values.
