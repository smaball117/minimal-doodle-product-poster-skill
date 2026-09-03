# Lettering Layer Prompt

Prompt revision: **v0.9-semantic-cluster-lettering**

Use only after the poster base is accepted in Fidelity Mode.

```text
Create only the exact Chinese title below as a separate lettering layer.

TEXT, EXACT:
“[caption]”

SEMANTIC RULE
Preserve the exact characters and natural reading order. Do not add, delete, replace, translate, or romanize any character.

SEMANTIC CLUSTER PLAN
Before drawing, split the caption into natural phrase clusters.

Examples:
- 心态放苹 → 心态 / 放苹
- 焦糖脑袋冲啊 → 焦糖 / 脑袋 / 冲啊
- 清甜下午茶 → 清甜 / 下午茶

Use the most natural grouping for the actual caption. Do not mechanically isolate every character.

CORE RULE
The result must feel like one compact handwritten title made of loose phrase clusters.
Do NOT typeset the whole caption as one clean sentence line.
Do NOT scatter every character as an isolated sticker.

STYLE
Thin black naive handwriting. Characters should feel written by hand rather than typeset: uneven size, independent mild tilt, loose internal structure, slightly stretched or compressed radicals, occasional elongated horizontal strokes, blunt simple stroke endings, mild natural wobble, readable Chinese with human imperfection.

GLYPH SKELETON
Do not keep a clean standard typeface skeleton underneath. Vary character box, tilt, internal spacing, radical proportions, and horizontal-stroke length while keeping every character recognizable.

CLUSTER SPACING LOCK
- characters inside the same semantic cluster stay relatively close;
- within-cluster spacing may vary slightly but must still read as one phrase unit;
- gaps between clusters should usually be about 1.4–2.2× the typical within-cluster gap;
- each cluster may have its own slight x/y offset and baseline drift;
- cluster members may differ slightly in size and tilt;
- no perfect shared baseline across all clusters;
- preserve clear reading order.

COMPACT TITLE BLOCK
For 4–6 characters, keep the overall lettering as one compact note block in roughly:
- 20%–35% of canvas width;
- 15%–28% of canvas height.

Do not create:
- a long diagonal chain across the canvas;
- one character per row;
- a huge title footprint competing with the product;
- a rigid rectangle.

LENGTH ROUTING
If caption length = 2:
- one loose cluster;
- slight size, spacing, and baseline mismatch.

If caption length = 3:
- one cluster or natural 2+1 grouping;
- compact, not an evenly spaced straight row.

If caption length = 4:
- use 2 semantic clusters when natural;
- loose two-level arrangement;
- never a perfect 2×2 grid;
- do not isolate all 4 characters.

If caption length = 5–6:
- use 2–3 semantic clusters;
- cluster members stay close;
- cluster gaps stay larger;
- no continuous typeset line;
- no all-character isolation;
- no regular diagonal staircase.

If caption length >= 7:
- split into natural groups of about 2–3 characters;
- keep group members close and overall title compact.

AVOID
No brush calligraphy, elegant handwriting, rounded cute font, sans-serif font, standard system typography, perfect grid, equal spacing, one-character-per-row isolation, long diagonal staircase, identical character boxes, commercial poster font, pinyin, English, numbers, extra characters, logo, watermark.

OUTPUT
Only the black handwritten Chinese title on a plain white or transparent background. No product, no workers, no arrows, no decorative graphics.
```

## Repair pass

If glyphs are correct but the title is too fragmented:

1. keep the poster base unchanged;
2. keep the existing glyph style;
3. regroup the exact text into natural semantic clusters;
4. move members of each cluster closer together;
5. increase gaps between clusters;
6. remove one-character-per-row isolation;
7. compress the entire title into one compact handwritten block;
8. preserve slight baseline, size, tilt, and spacing variation.

If the title is too typeset, preserve the semantic clusters but loosen x/y position, baseline, local scale, and spacing.

Do not solve a lettering-only defect by regenerating the photographic poster base.