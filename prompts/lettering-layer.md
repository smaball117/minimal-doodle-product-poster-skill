# Lettering Layer Prompt

Prompt revision: **v0.8-lettering-spatial-rhythm**

Use only after the poster base is accepted in Fidelity Mode.

```text
Create only the exact Chinese text below as a separate lettering layer.

TEXT, EXACT:
“[caption]”

SEMANTIC RULE
Preserve the exact characters and natural reading order. Do not add, delete, replace, translate, or romanize any character.

CORE RULE
Do NOT typeset the text as one phrase.
Treat every Chinese character as an individually placed handwritten object.

STYLE
Thin black naive handwriting. Characters should feel written by hand rather than typeset: uneven character sizes, independent mild tilt, loose internal structure, slightly stretched or compressed radicals, occasional elongated horizontal strokes, blunt simple stroke endings, mild natural wobble, readable Chinese with obvious human imperfection.

GLYPH SKELETON
Do not keep a clean standard typeface skeleton underneath. Vary each character box, tilt, internal spacing, radical proportions, and horizontal-stroke length. Keep every character recognizable.

SPATIAL RHYTHM LOCK
Before rendering, assign each character its own x/y position.

Required:
- no single shared baseline;
- no equal character tracking;
- adjacent gaps must be visibly different;
- at least one gap should be about 1.5–2.5× another nearby gap;
- at least one character must sit clearly higher or lower than another;
- use loose off-grid placement;
- reading order remains understandable;
- avoid a rectangular text block.

LENGTH ROUTING
If caption length = 2 characters:
- loose horizontal placement is allowed;
- use unequal spacing and baseline mismatch.

If caption length = 3 characters:
- prefer diagonal, triangular, or stair-step placement;
- do not use one straight row.

If caption length = 4 characters:
- use a loose staggered two-level structure;
- never use a perfect 2×2 grid.

If caption length = 5–6 characters:
- split into 2–3 loose character clusters;
- never render the entire caption as one continuous line;
- cluster gaps must be larger than within-cluster gaps;
- use different x/y offsets for each cluster.

If caption length >= 7 characters:
- divide into semantic groups of about 2–3 characters;
- place groups on staggered levels;
- preserve reading order without forming a neat text block.

AVOID
No brush calligraphy, elegant handwriting, rounded cute font, sans-serif font, standard system typography, perfect grid, equal spacing, aligned columns, shared baseline, identical character boxes, commercial poster font, pinyin, English, numbers, extra characters, logo, watermark.

OUTPUT
Only the black handwritten Chinese characters on a plain white or transparent background. No product, no workers, no arrows, no decorative graphics.
```

## Repair pass

If glyphs look handwritten but the phrase still feels typeset, do NOT alter the poster base and do NOT mainly change stroke texture.

Repair only spatial rhythm:

1. re-place every character independently;
2. break the shared baseline;
3. vary x/y position;
4. vary character scale;
5. make adjacent gaps visibly unequal;
6. split 5–6 characters into 2–3 loose clusters;
7. preserve exact text and reading order.

If glyph skeleton is also too font-like, additionally vary radical proportions, internal spaces, tilt, and horizontal-stroke length.

Do not solve a lettering-only defect by regenerating the photographic poster base.