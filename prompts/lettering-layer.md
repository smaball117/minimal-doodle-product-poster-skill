# Lettering Layer Prompt

Use only after the poster base is accepted in Fidelity Mode.

```text
Create only the exact Chinese phrase below as a separate lettering layer.

TEXT, EXACT:
“[caption]”

STYLE
Thin black naive handwriting. The characters should feel written by hand rather than typeset: uneven character sizes, slight independent tilt, irregular spacing, off-grid placement, loose internal structure, slightly stretched or compressed radicals, occasional elongated horizontal strokes, blunt simple stroke endings, mild natural wobble, readable Chinese with obvious human imperfection.

GLYPH SKELETON
Do not keep a clean standard typeface skeleton underneath. Vary each character box, x/y position, tilt, internal spacing, radical proportions, and horizontal-stroke length. Keep the phrase recognizable and readable.

AVOID
No brush calligraphy, no elegant handwriting, no rounded cute font, no sans-serif font, no standard system typography, no perfect grid, no identical character boxes, no commercial poster font, no pinyin, no English, no numbers, no extra characters, no logo, no watermark.

OUTPUT
Only the black handwritten phrase on a plain white or transparent background. No product, no workers, no arrows, no decorative graphics.
```

## Repair pass

If the result still looks font-like, keep the poster base unchanged and regenerate only this layer with stronger glyph-skeleton variation.

Prioritize:

1. different character sizes;
2. different tilt angles;
3. different x/y offsets;
4. irregular internal spaces;
5. stretched/compressed radical proportions;
6. longer or shorter horizontal strokes;
7. thin black hand-line consistency.

Do not solve a lettering-only defect by regenerating the photographic poster base.