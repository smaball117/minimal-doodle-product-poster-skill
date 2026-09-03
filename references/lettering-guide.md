# Lettering Guide

Revision: **v0.8-lettering-spatial-rhythm**

## Goal

The target Chinese lettering is not a normal font with a rough texture added. It should feel handwritten, naive, loose, thin, awkward, slightly untrained, and **spatially placed by hand** while remaining readable.

The key distinction is:

> Do not typeset a phrase. Place every Chinese character individually.

## Five-layer model

Think about lettering in five layers:

1. **Semantic text**: exact characters and reading order.
2. **Glyph skeleton**: character proportions, radical structure, tilt, deformation.
3. **Stroke surface**: thin black pen line, mild wobble, blunt endings.
4. **Character placement**: each character gets its own x/y position and local scale.
5. **Phrase rhythm**: uneven gaps, broken baselines, loose clusters, visual breathing.

A title can have correct handwriting strokes and still fail if layers 4–5 look typeset.

## Visual anatomy

Use these traits:

- thin black single-line strokes;
- slight natural hand wobble;
- independent character tilt;
- intentionally inconsistent character sizes;
- no shared perfect baseline;
- clearly uneven horizontal and vertical gaps;
- some horizontal strokes may extend unusually long;
- radicals and inner spaces may stretch, compress, or shift off-center;
- blunt simple stroke endings;
- the whole title feels written directly into the blank space, not laid out by software.

## Spatial Rhythm Lock

Before rendering the lettering, plan each Chinese character as an independent object.

Required:

- each character has its own x/y position;
- adjacent character gaps must be visibly different;
- at least one gap should be roughly **1.5–2.5×** another nearby gap;
- at least one character must sit noticeably higher or lower than another;
- characters must not share a single clean baseline;
- avoid equal tracking, equal line spacing, aligned columns, or repeated character boxes;
- reading order must remain understandable even when the layout is staggered.

The result should feel like a person wrote several characters one by one and let the composition drift naturally.

## Layout rules by caption length

### 2 characters

- horizontal placement is allowed;
- do not use equal spacing;
- use slight size and baseline mismatch.

### 3 characters

- prefer triangular, diagonal, or stair-step placement;
- avoid one straight row.

### 4 characters

- prefer a loose two-level or staggered structure;
- **never use a perfect 2×2 grid**;
- do not align both rows to the same left/right edges.

### 5–6 characters

- split into **2–3 loose semantic/spatial clusters**;
- do not render the full caption as one continuous line;
- cluster gaps should be larger than within-cluster gaps;
- keep irregular x/y offsets between groups.

Example concept for `焦糖脑袋冲啊`:

```text
焦      糖
    脑
袋         冲
     啊
```

This is a rhythm example, not a fixed template.

### 7+ characters

- divide into readable semantic groups of roughly 2–3 characters;
- place groups on staggered levels;
- preserve natural reading order without forming a neat text block.

## Avoid

- standard system fonts;
- sans-serif / hei-ti appearance;
- song-ti appearance;
- brush calligraphy;
- elegant handwriting;
- rounded cute fonts;
- neat commercial typography;
- one clean text row for 5+ characters;
- perfect grids;
- identical character boxes;
- equal character tracking;
- uniform line spacing;
- shared baselines;
- aligned columns;
- decorative English, pinyin, numbers, or extra glyphs.

## Caption writing

Preferred length: 2–6 Chinese characters, but slightly longer short phrases are acceptable when supplied by the user.

Good tone:

- conversational;
- light;
- product-inspired;
- gentle wordplay when natural;
- not a hard-sell slogan.

Examples:

- 补水中
- 今天有点甜
- 请勿打扰
- 清甜下午茶
- 清爽营业中

## Poster placement

Text participates in composition instead of behaving like a formal title block.

Typical placement:

- upper-left;
- left side;
- loose staggered clusters;
- paired with one simple curved arrow when useful.

Leave breathing space around the title. Do not pack the characters tightly into a rectangle.

## Quick Mode

For one-pass generation, inline both handwriting style and spatial rhythm:

```text
Treat every Chinese character as an individually placed handwritten object, not a typeset phrase. Use thin black naive handwriting, uneven character sizes, independent tilt, different x/y positions, broken baselines, visibly unequal gaps, and loose staggered clusters. For 5–6 characters, split into 2–3 loose groups and never render the whole caption as one continuous line.
```

## Fidelity Mode

Use when lettering is the defect or when high resemblance is important.

### Pass 1
Generate poster base with a clean empty title area.

### Pass 2
Generate only the exact Chinese characters as a lettering layer using both glyph-skeleton and spatial-rhythm rules.

### Pass 3
Composite the accepted title layer onto the unchanged poster base.

Do not regenerate the photographic poster just to fix typography.

## Repair instruction

If the glyphs look handwritten but the phrase still feels typeset:

```text
Keep the poster base unchanged. Repair only the lettering layer. Do not rewrite the characters as one phrase. Re-place each Chinese character independently. Break the shared baseline, vary x/y position and local scale, make adjacent gaps visibly unequal, and split 5–6 characters into 2–3 loose clusters. Preserve the exact text and reading order.
```

If the lettering still looks like a computer font, also vary glyph box size, tilt, internal spacing, radical proportions, and horizontal-stroke length.

## Reference-image learning

When handwriting references are supplied, extract reusable traits such as:

- stroke thinness;
- character tilt;
- spacing rhythm;
- relative scale variation;
- x/y drift;
- baseline breaks;
- elongated horizontal strokes;
- loose radical construction.

Do not redistribute third-party reference images as repository assets without permission.