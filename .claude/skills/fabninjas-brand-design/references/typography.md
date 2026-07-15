# FabNinjas Typography

**Source:** `FabNinjas_BrandGuidelines.pdf`, page 4 — *"Font That Brings Our Story Alive."*

## The typeface

**Libre Franklin** is the *only* brand typeface. It carries all display, heading, and
body text. (The "fab" wordmark is hand-lettered art, not type — see `logo-usage.md`.)

- Full character set is approved: `a–z A–Z 0123456789 ,.;':"<>?[]{}\|!@#$%^&*()-=_+`~`
- Libre Franklin ships a full weight range (Thin 100 → Black 900, plus italics).

## Rules to live by (verbatim from the source — enforce exactly)

1. **Never distort the font in any shape or form** — no horizontal/vertical scaling,
   no stretching, condensing, skewing, or outlining to fake a weight.
2. **Tracking = 0, leading = auto** by default. Only depart from this when a specific
   use genuinely calls for it; never track/letterspace body copy.
3. **Use the full family, combined wisely** — build hierarchy by pairing *real* weights
   (e.g. Black headline over Regular body), not by distorting one weight.

## Weight usage (recommendation — the source names no scale)

The guidelines mandate the family and the "combine wisely" rule but give no type scale.
Sensible defaults, consistent with how the source sets its own pages:

| Level         | Weight                | Notes |
|---------------|-----------------------|-------|
| Display / H1  | Libre Franklin **Black / ExtraBold**, uppercase | Matches the "ABOUT US / COLOURS" page titles |
| Subhead       | Libre Franklin **Medium Italic** | The source pairs an italic subhead beside the title |
| Body          | Libre Franklin **Regular** | Tracking 0, leading auto (~1.4–1.5× for screen) |
| Emphasis      | Libre Franklin **SemiBold** | Prefer weight over italics/underline for emphasis |
| Caption / meta| Libre Franklin **Regular/Medium**, smaller | — |

Treat the table as a starting point, not a mandate; the binding rules are the three above.

## Getting the font

The brand folder ships no font files — the source names the typeface only. Libre Franklin
is free and open-source, so install it from the canonical source:

- Google Fonts: https://fonts.google.com/specimen/Libre+Franklin
- Licence: SIL Open Font License 1.1 (free to embed and redistribute).
- Web CSS: `font-family: "Libre Franklin", sans-serif;` — load via the Google Fonts link
  or a self-hosted `@font-face`. Always include the `sans-serif` fallback so nothing
  renders in a serif if the font fails to load.
- Libre Franklin ships as a **variable** font: one file covers every weight via
  `font-weight: 100–900`, plus a matching italic.

## Do / Don't

- **Do** set everything in Libre Franklin; build hierarchy with real weights.
- **Do** keep tracking at 0 and leading auto for body copy.
- **Don't** substitute Arial/Helvetica/Inter etc. as a "close enough" font.
- **Don't** stretch, condense, skew, or outline the type.
- **Don't** letterspace or tighten body text to make it fit — change size or copy instead.
