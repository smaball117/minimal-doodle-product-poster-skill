# Evaluation Guide

Revision: **v0.7-worker-scale-calibration**

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

Fail when workers have giant heads, barrel-shaped bodies, thick stubby limbs, long fashion-like limbs, or adult stick-figure anatomy.

## E. Worker relative scale

- [ ] Normal worker visual height is about **12%–18% of hero height**.
- [ ] Preferred average is about **14%–16%**.
- [ ] No worker exceeds **20% of hero height** without explicit user request.
- [ ] Product visually dominates before any worker is noticed.
- [ ] Workers on/behind the product may be smaller or partially occluded.

If workers feel like co-equal characters, they are too large.

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

## H. Lettering

When text is used:

- [ ] Exact requested wording is attempted without extra copy.
- [ ] Thin black line handwriting.
- [ ] Character sizes, tilt, spacing, and baselines are irregular.
- [ ] Does not look like standard computer typography.
- [ ] Not brush calligraphy, rounded cute handwriting, or polished commercial lettering.
- [ ] Text participates in composition rather than forming a formal ad block.

When typography is the only failure, use `fidelity_focus: lettering` and keep the poster base unchanged.

## I. Palette

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
- [ ] Workers interact with the focus before secondary elements.

### lettering

- [ ] Accepted poster base remains unchanged.
- [ ] Only lettering layer changes.
- [ ] Glyph skeleton, spacing, tilt, scale, or baseline issues are repaired.

## Known failure modes

### 1. Product drift

Example: blue pudding becomes shaved ice.

Repair: lock category, silhouette, material, color, topping, and support relation.

### 2. Character drift

Workers gain faces, clothes, hats, badges, or mascot styling.

Repair: reassert fixed faceless worker identity.

### 3. Chibi overcorrection

Example: workers become giant-headed, fat, barrel-bodied, or thick-limbed after trying to avoid stick figures.

Cause: silhouette lock overemphasized “squat / oversized head / stubby limbs”.

Repair: recalibrate to 2.8–3.5 heads tall, head 28%–35%, torso width 55%–75% of head diameter, slim short-to-medium limbs.

### 4. Worker scale inflation

Example: workers are stylistically correct but too large compared with the product.

Cause: anatomy was constrained but relative product-to-worker scale was not.

Repair: enforce 12%–18% hero-height target, preferred 14%–16%, max 20%.

### 5. Stick-figure drift

Workers become tall, thin, long-limbed doodle humans.

Repair: use compact 2.8–3.5-head geometry with narrow rounded torso and slim short-to-medium limbs.

### 6. Default ladder repetition

Ladders repeatedly appear even when unnecessary.

Repair: structural-prop budget defaults to 0 and is capped at 1. Use ladder only for meaningful vertical access.

### 7. Floating ladder / prop

Repair: require visible base support, matching perspective, stable top contact, and worker contact. Otherwise remove it.

### 8. Weak worker story

A worker merely waves or decorates.

Repair: delete or replace with a product-feature action.

### 9. Font-like handwriting

Repair lettering layer only; vary glyph boxes, tilt, spacing, radical proportions, and horizontal stroke lengths.

### 10. Too much decoration

Remove half of supporting doodles and restore blank space.

### 11. Dominant-focus dilution

Demote secondary scene cues in scale, contrast, saturation, and placement.

### 12. Multi-case blending

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
9. If text exists, does it feel written rather than typeset?
10. What single defect should be repaired next?

## Regression policy

Any repeatable failure should become an eval case in `evals/evals.json`. Do not optimize only around one pretty example.