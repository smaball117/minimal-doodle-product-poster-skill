# Lettering Guide

## Goal

The target Chinese lettering is not a normal font with a rough texture added. It should feel handwritten, naive, loose, thin, awkward, and slightly untrained while remaining readable.

## Visual anatomy

Use these traits:

- thin black single-line strokes;
- slightly shaky hand pressure;
- characters may tilt independently;
- character sizes are intentionally inconsistent;
- baselines do not align perfectly;
- spacing is loose and irregular;
- some horizontal strokes may extend unusually long;
- radicals and inner spaces can be slightly stretched, compressed, or off-center;
- stroke endings are plain and blunt rather than calligraphic;
- the whole phrase feels placed by hand, not typeset.

## Avoid

- standard system fonts;
- sans-serif / hei-ti appearance;
- song-ti appearance;
- brush calligraphy;
- elegant handwriting;
- rounded cute fonts;
- neat commercial typography;
- perfect grids;
- identical character boxes;
- consistent stroke width with vector-clean edges;
- decorative English, pinyin, numbers, or extra glyphs.

## Important distinction: skeleton vs surface

When lettering looks too much like a computer font, adding more words such as “handwritten”, “rough”, or “childlike” often does not solve the real problem.

Think in four layers:

1. **Semantic text**: exact characters that must be written.
2. **Glyph skeleton**: each character’s proportions, tilt, spacing, malformed-but-readable structure.
3. **Stroke surface**: thin black pen line, slight wobble, blunt ends, small pressure changes.
4. **Poster placement**: loose off-grid positioning inside negative space.

The most common failure is layer 2: the model keeps a standard font skeleton underneath.

## Caption writing

Preferred length: 2–6 Chinese characters, but slightly longer short phrases are acceptable when the user provides them.

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

Shorter text reduces generation errors.

## Layout

Text participates in composition instead of behaving like a formal title block.

Typical placement:

- upper-left;
- left side;
- occasionally split into loose lines or staggered columns;
- paired with one simple curved arrow.

For four-character text, avoid a perfect 2×2 grid. Prefer loose staggered placement with different character sizes and vertical gaps.

## Quick Mode

For draft generation, text may be generated together with the poster.

Prompt emphasis:

```text
thin black naive handwriting, loose and awkward, uneven character sizes, mild tilt, irregular spacing, occasional elongated horizontal strokes, readable Chinese but clearly not typeset
```

## Fidelity Mode

Use when the user says the font is wrong or wants high resemblance.

### Pass 1

Generate the poster base with a clean empty title area. No text at all.

### Pass 2

Generate only the exact Chinese phrase on white or transparent background.

### Pass 3

Composite the accepted title layer onto the unchanged poster base.

Do not keep regenerating the entire poster just to fix typography.

## Title-layer prompt principle

```text
Create only the exact Chinese phrase as thin black naive handwriting. Keep every character readable, but make the glyph skeleton visibly hand-built: uneven size, slight independent tilt, irregular spacing, off-grid placement, stretched or compressed internal structure, occasional elongated horizontal strokes, blunt simple line endings, no calligraphy rhythm, no rounded cute font, no clean standard font skeleton.
```

## Repair instruction

If the title still looks like a normal font:

```text
Keep the poster base unchanged. Regenerate only the lettering layer. Focus on glyph skeleton deformation rather than adding rough texture: vary character box size, tilt, x/y position, internal spacing, radical proportions, and horizontal stroke length. Keep thin black pen strokes. Reject standard typeface skeletons, neat grids, calligraphy, rounded cute handwriting, and polished commercial typography.
```

## Reference-image learning

When handwriting references are supplied, extract only reusable traits such as:

- stroke thinness;
- character tilt;
- spacing rhythm;
- relative scale variation;
- elongated horizontal strokes;
- loose radical construction.

Do not treat third-party reference images as public assets to be redistributed by the repository.