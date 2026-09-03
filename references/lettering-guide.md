# Lettering Guide

Revision: **v0.9-semantic-cluster-lettering**

## Goal

The target Chinese lettering is not a normal font with a rough texture added. It should feel handwritten, naive, loose, thin, awkward, slightly untrained, and naturally grouped by meaning while remaining readable.

The key distinction is:

> Do not typeset the whole sentence as one line. Do not scatter every character as an isolated sticker. Group by meaning first, then loosen the spacing.

## Five-layer model

Think about lettering in five layers:

1. **Semantic text**: exact characters and natural reading order.
2. **Semantic clustering**: which characters naturally belong together as a phrase unit.
3. **Glyph skeleton**: character proportions, radical structure, tilt, deformation.
4. **Stroke surface**: thin black pen line, mild wobble, blunt endings.
5. **Spatial rhythm**: compact cluster placement, unequal gaps, broken baselines, breathing space.

A title can have correct handwriting strokes and still fail if it is either too typeset or too fragmented.

## Semantic Cluster Lock

Before rendering, split the caption into natural phrase groups.

Examples:

- `心态放苹` → `心态` / `放苹`
- `焦糖脑袋冲啊` → `焦糖` / `脑袋` / `冲啊`
- `清甜下午茶` → `清甜` / `下午茶`
- `今天有点甜` → `今天` / `有点甜`

Use semantic grouping rather than mechanical character splitting.

### Within-cluster behavior

- characters in the same cluster stay relatively close;
- they may still vary in size, tilt, and baseline;
- spacing should feel handwritten, not mechanically equal;
- the cluster must still read as one phrase unit.

### Between-cluster behavior

- gaps between clusters should normally be about **1.4–2.2×** the typical within-cluster gap;
- clusters may shift slightly in x/y position;
- cluster baselines should not align perfectly;
- clusters can form a loose two-level or three-level handwritten block.

## Compact Title Block Lock

The whole title should remain visually compact in the upper-left or left-side negative space.

For 4–6 characters, use these guidance ranges:

- title block width: about **20%–35% of canvas width**;
- title block height: about **15%–28% of canvas height**.

The exact size may vary, but avoid:

- a long diagonal chain of isolated characters;
- one-character-per-row layouts;
- a title spreading across half the canvas;
- a rigid rectangular typesetting block.

The title should feel like a small handwritten note, not an infographic path.

## Visual anatomy

Use these traits:

- thin black single-line strokes;
- slight natural hand wobble;
- independent character tilt;
- intentionally inconsistent character sizes;
- no shared perfect baseline;
- clearly uneven gaps;
- some horizontal strokes may extend unusually long;
- radicals and inner spaces may stretch, compress, or shift off-center;
- blunt simple stroke endings;
- the whole title feels written directly into blank space.

## Layout rules by caption length

### 2 characters

- one loose cluster;
- horizontal placement allowed;
- use slight size, tilt, and baseline mismatch.

### 3 characters

- one loose cluster or a natural 2+1 grouping;
- compact placement;
- avoid a perfectly straight, evenly spaced row.

### 4 characters

- default to **2 semantic clusters** when natural;
- example: `心态` / `放苹`;
- use a loose two-level arrangement;
- never use a perfect 2×2 grid;
- do not isolate all four characters from each other.

### 5–6 characters

- default to **2–3 semantic clusters**;
- example: `焦糖` / `脑袋` / `冲啊`;
- keep cluster members visibly closer than cluster-to-cluster gaps;
- do not render the whole caption as one clean line;
- do not scatter all characters as independent points;
- avoid a regular diagonal staircase.

### 7+ characters

- split into natural semantic groups of roughly 2–3 characters;
- keep group members close and overall title block compact;
- preserve reading order without forming a clean paragraph block.

## Avoid

- standard system fonts;
- sans-serif / hei-ti appearance;
- song-ti appearance;
- brush calligraphy;
- elegant handwriting;
- rounded cute fonts;
- neat commercial typography;
- one clean sentence line for long captions;
- every character isolated from all others;
- one-character-per-row layout;
- long diagonal stair-step chain;
- perfect grids;
- identical character boxes;
- equal character tracking;
- uniform line spacing;
- aligned columns;
- decorative English, pinyin, numbers, or extra glyphs.

## Poster placement

Typical placement:

- upper-left;
- left side;
- compact staggered phrase clusters;
- paired with one simple curved arrow when useful.

The arrow should visually depart from the title block as a whole, usually from the lower or side edge, rather than from one randomly isolated final character.

## Quick Mode

For one-pass generation, inline both handwriting style and semantic clustering:

```text
First split the exact Chinese caption into natural semantic clusters. Keep characters inside each cluster relatively close, and make gaps between clusters clearly larger. Let clusters drift slightly in x/y position and baseline, but keep the whole title compact in the upper-left whitespace. Use thin black naive handwriting with irregular glyph skeleton, size, tilt, and spacing. Do not typeset the entire caption as one clean line and do not scatter every character as an isolated sticker.
```

## Fidelity Mode

Use when lettering is the defect or when high resemblance is important.

### Pass 1
Generate poster base with a clean empty title area.

### Pass 2
Generate only the exact Chinese title layer using semantic clusters + glyph + spatial rules.

### Pass 3
Composite the accepted title layer onto the unchanged poster base.

Do not regenerate the photographic poster just to fix typography.

## Repair instruction

If glyphs look right but the title is too fragmented:

```text
Keep the poster base and glyph style unchanged. Repair only the lettering placement. Regroup the exact text into natural semantic clusters. Move characters within each cluster closer together, enlarge gaps between clusters, remove one-character-per-row isolation, and compress the whole title into one compact handwritten block. Preserve irregular size, tilt, baseline, and readable order.
```

If the title is too typeset:

```text
Keep semantic clusters intact, then loosen them: break shared baselines, vary x/y placement, local scale, tilt, and within-cluster spacing. Keep cluster members closer than cluster-to-cluster gaps.
```

If glyph skeleton is also too font-like, vary radical proportions, internal spaces, tilt, and horizontal-stroke length.

## Reference-image learning

When handwriting references are supplied, extract reusable traits such as:

- stroke thinness;
- semantic grouping rhythm;
- within-cluster closeness;
- between-cluster breathing;
- character tilt;
- relative scale variation;
- baseline breaks;
- elongated horizontal strokes;
- loose radical construction.

Do not redistribute third-party reference images as repository assets without permission.