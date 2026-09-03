# Evaluation Guide

Revision: **v0.8-lettering-spatial-rhythm**

Use after every generated poster and after every major Skill revision.

## A. Subject fidelity

- [ ] Exact source category is preserved.
- [ ] Original silhouette and proportions remain recognizable.
- [ ] Main color and material remain faithful.
- [ ] Defining toppings/container/support relation remain when necessary.
- [ ] Product remains photographic, not illustrated or cartoonized.

## B. Composition

- [ ] One hero object dominates the photographic layer.
- [ ] White / warm-white negative space remains generous.
- [ ] Product is noticed before workers.
- [ ] Workers do not form an evenly spaced decorative ring.
- [ ] No dense commercial-ad clutter appears.

Default negative-space target: about 70%–80%. In `dominant_element` Fidelity passes, 60%–70% is acceptable.

## C. Micro-worker identity

- [ ] Blank round or slightly irregular heads.
- [ ] No eyes, mouth, facial expression, hair, hats, or clothing details.
- [ ] No labels, logos, badges, or body symbols.
- [ ] White empty interiors.
- [ ] Black thin uneven hand-drawn outlines.
- [ ] No polished mascot treatment.

## D. Worker silhouette calibration

- [ ] Total figure height is about **2.8–3.5 head diameters**.
- [ ] Head occupies about **28%–35%** of total figure height.
- [ ] Torso width is about **55%–75% of head diameter**.
- [ ] Torso is lightly rounded but not broad/barrel-shaped.
- [ ] Arms and legs are slim and short-to-medium.
- [ ] Workers do not look fat/chibi.
- [ ] Workers do not look like tall adult stick figures.

## E. Worker relative scale

- [ ] Normal worker visual height is about **12%–18% of hero height**.
- [ ] Preferred average is about **14%–16%**.
- [ ] No worker exceeds **20% of hero height** without explicit user request.
- [ ] Product visually dominates before any worker is noticed.

## F. Worker action

- [ ] Every worker has a clear action verb.
- [ ] Every action relates to a real product feature.
- [ ] At least three workers have readable contact or cause-and-effect with the product.
- [ ] Removing any worker would remove a layer of product meaning.

## G. Structural props

- [ ] Default structural-prop count is 0.
- [ ] Maximum structural-prop count is 1.
- [ ] A ladder/stool/step appears only when vertical access materially improves the story.
- [ ] Structural prop base visibly rests on the ground plane.
- [ ] Perspective matches the scene.
- [ ] Worker hands/feet connect to the prop.
- [ ] No structural prop floats or terminates in empty space.
- [ ] No rope, scaffold, suspended line, or floating platform appears unless explicitly requested.

A grounded single ladder is acceptable; repeated or unnecessary ladders are not.

## H. Lettering glyph style

When text is used:

- [ ] Exact requested wording is present without extra copy.
- [ ] Thin black line handwriting.
- [ ] Character sizes and tilt are visibly irregular.
- [ ] Glyph skeletons do not look like a standard font.
- [ ] No brush calligraphy, rounded cute handwriting, or polished commercial lettering.

## I. Lettering spatial rhythm

This is a separate check from glyph style.

- [ ] Characters are treated as individually placed handwritten objects, not one typeset phrase.
- [ ] No single clean shared baseline dominates the title.
- [ ] Adjacent gaps are visibly unequal.
- [ ] At least one gap is roughly 1.5–2.5× another nearby gap.
- [ ] At least one character sits noticeably higher or lower than another.
- [ ] Character x/y positions drift naturally while reading order remains clear.
- [ ] The title does not form a neat rectangle, aligned columns, or a repeated grid.

Length-specific checks:

- [ ] 2 chars: unequal spacing + baseline mismatch.
- [ ] 3 chars: not one straight row; diagonal / triangular / stair-step is acceptable.
- [ ] 4 chars: not a perfect 2×2 grid.
- [ ] 5–6 chars: split into 2–3 loose clusters; **not one continuous line**.
- [ ] 7+ chars: semantic groups are staggered instead of forming a clean paragraph block.

When glyphs are correct but spacing still feels typeset, use `fidelity_focus: lettering` and repair only spatial rhythm.

## J. Palette

- [ ] Colors come from source subject plus white and black.
- [ ] No unrelated accent color is added without user request.

## Fidelity Focus checks

### subject_identity

- [ ] Result is unmistakably the same photographed object without text.
- [ ] Category, silhouette, material, color, and defining details survive.
- [ ] Creative exaggeration does not alter product identity.

### dominant_element

- [ ] Focus element was explicitly identified before generation.
- [ ] Selected focus is the first photographic signal at thumbnail size.
- [ ] It is the largest meaningful subject element, not background architecture.
- [ ] Secondary cues remain clearly weaker.
- [ ] Workers interact with focus before secondary elements.

### lettering

- [ ] Accepted poster base remains unchanged.
- [ ] Only lettering layer changes.
- [ ] Exact wording remains intact.
- [ ] Glyph skeleton or spatial rhythm defects are repaired without regenerating product/workers.

## Known failure modes

### 1. Product drift

Example: blue pudding becomes shaved ice.

Repair: lock category, silhouette, material, color, topping, and support relation.

### 2. Character drift

Workers gain faces, clothes, hats, badges, or mascot styling.

Repair: reassert fixed faceless worker identity.

### 3. Chibi overcorrection

Workers become giant-headed, fat, barrel-bodied, or thick-limbed.

Repair: recalibrate to 2.8–3.5 heads tall, head 28%–35%, torso width 55%–75% of head diameter, slim short-to-medium limbs.

### 4. Worker scale inflation

Workers are stylistically correct but too large relative to the product.

Repair: enforce 12%–18% hero-height target, preferred 14%–16%, max 20%.

### 5. Stick-figure drift

Workers become tall, thin, long-limbed doodle humans.

Repair: use compact 2.8–3.5-head geometry with narrow rounded torso and slim short-to-medium limbs.

### 6. Default ladder repetition

Ladders repeatedly appear even when unnecessary.

Repair: structural-prop budget defaults to 0 and is capped at 1.

### 7. Floating ladder / prop

Repair: require visible base support, matching perspective, stable contact, and worker contact. Otherwise remove it.

### 8. Weak worker story

A worker merely waves or decorates.

Repair: delete or replace with a product-feature action.

### 9. Font-like glyph skeleton

Letters look like a standard font with rough texture.

Repair: regenerate lettering only; vary glyph boxes, tilt, internal spacing, radical proportions, and stroke lengths.

### 10. Typeset spacing drift

Example: `焦糖脑袋冲啊` has acceptable handwritten glyphs but appears as one evenly spaced horizontal sentence.

Cause: the model treated the title as a phrase-level text object instead of individually placed characters.

Repair: keep glyph style and poster base. Re-place every character independently. Break shared baseline, vary x/y position, make gaps unequal, and split 5–6 characters into 2–3 loose clusters.

### 11. Perfect-grid handwriting

Example: four characters are placed in a neat 2×2 square.

Repair: offset character positions, change local scale, break row/column alignment, and create a loose staggered two-level rhythm.

### 12. Too much decoration

Remove half of supporting doodles and restore blank space.

### 13. Dominant-focus dilution

Demote secondary scene cues in scale, contrast, saturation, and placement.

### 14. Multi-case blending

Process each source as an independent generation unless a comparison board is explicitly requested.

## Review questions

1. Is the product unmistakably the same object?
2. Is the product the first visual signal?
3. Are workers small enough relative to the hero?
4. Are workers neither chubby/chibi nor long-limbed stick figures?
5. Does each worker action map to a real product feature?
6. Is any ladder/stool genuinely useful and physically grounded?
7. Is structural-prop count at most one?
8. Is white space doing compositional work?
9. Are the handwritten glyphs correct?
10. Does the title feel placed character-by-character rather than typeset as a phrase?
11. For 5–6 characters, is the caption broken into loose clusters rather than one line?
12. What single defect should be repaired next?

## Regression policy

Any repeatable failure should become an eval case in `evals/evals.json`. Do not optimize only around one pretty example.