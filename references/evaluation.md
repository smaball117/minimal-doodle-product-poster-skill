# Evaluation Guide

Use this after every generated poster and after every major Skill revision.

## Pass criteria

### A. Subject fidelity

- [ ] The exact source category is preserved.
- [ ] The original silhouette and proportions are recognizable.
- [ ] Main color and material remain faithful.
- [ ] Important toppings, garnish, plate, cup, bottle, or support relation are preserved when defining.
- [ ] The product remains photographic, not illustrated or 3D-cartoonized.

### B. Composition

- [ ] One hero object dominates the photographic layer.
- [ ] White / warm-white negative space remains generous.
- [ ] The object sits center-lower or another intentionally quiet lower position.
- [ ] Doodles do not evenly fill the blank field.
- [ ] No dense ad-layout clutter appears.

Default negative-space target is around 70%–80%. In `dominant_element` Fidelity passes, 60%–70% is acceptable when the larger focus needs more presence.

### C. Micro workers

- [ ] Workers use blank round heads.
- [ ] No eyes, mouths, facial expressions, hair, hats, or clothing details appear.
- [ ] No labels, logos, badges, or body symbols appear.
- [ ] Lines are black, simple, uneven, and hand-drawn.
- [ ] Every worker has a clear action verb.
- [ ] Every action relates to a real product feature.
- [ ] At least three workers have readable contact or cause-and-effect with the product.
- [ ] Removing any worker would remove a layer of product meaning.

Any visible face or designed costume is a fail, even when the overall poster looks good.

### D. Lettering

When text is used:

- [ ] Exact requested wording is attempted without extra copy.
- [ ] The lettering uses thin black lines.
- [ ] Character sizes, tilt, spacing, and baselines are irregular.
- [ ] The result does not look like standard computer typography.
- [ ] It is not brush calligraphy, rounded cute handwriting, or polished commercial lettering.
- [ ] Text participates in composition rather than forming a formal ad block.

When typography is the only failure, use `fidelity_focus: lettering` and keep the poster base unchanged.

### E. Palette

- [ ] Colors come from the source subject plus white and black.
- [ ] No unrelated accent color was added without user request.

## Fidelity Focus checks

Read `references/fidelity-focus.md` and evaluate the selected focus separately.

### subject_identity

- [ ] The result is unmistakably the same photographed object without relying on text.
- [ ] Category, silhouette, material, color, and defining details survive.
- [ ] Creative exaggeration does not alter product identity.
- [ ] Background cleanup does not remove essential support/container cues.

### dominant_element

- [ ] The focus element was explicitly identified before generation.
- [ ] The selected element is the first photographic signal at thumbnail size.
- [ ] It is the largest **meaningful subject element**, not irrelevant background architecture.
- [ ] Secondary photographic cues are limited to 0–2 when possible.
- [ ] Secondary elements do not compete through size, saturation, contrast, or central placement.
- [ ] Workers interact with the focus element before secondary elements.
- [ ] The focus remains realistic photography rather than becoming a cartoon prop.

### lettering

- [ ] The accepted poster base remains unchanged.
- [ ] Product, workers, lighting, and composition were not regenerated.
- [ ] Only the title layer changed.
- [ ] The new lettering fixes glyph skeleton, spacing, tilt, scale, or baseline issues.

## Known failure modes

### 1. Product drift

Example: blue pudding becomes shaved ice.

Cause: sensory concept overrode product identity.

Repair: lock category, silhouette, material, color, topping, and support relation before creative prompting.

### 2. Cute-character drift

Example: workers gain chef hats, faces, clothes, or expressions.

Cause: model interpreted “tiny workers” as designed characters.

Repair: reassert fixed figure contract and move storytelling into pose + tool only.

### 3. Weak worker story

Example: one worker waves while others do meaningful jobs.

Cause: worker count was treated as a quota.

Repair: delete the weak worker or replace it with a product-feature action.

### 4. Font-like handwriting

Cause: standard glyph skeleton remained underneath the “handwritten” texture.

Repair: keep poster base; regenerate only lettering layer; vary glyph boxes, tilt, spacing, radical proportions, and horizontal stroke lengths.

### 5. Too much decoration

Repair: remove half of supporting doodles, restore blank space, keep only action-serving marks.

### 6. Full illustration conversion

Repair: explicitly preserve real photographed material and studio-photography behavior.

### 7. Generic commercial poster

Repair: remove logos, frames, badges, price labels, grids, secondary copy, and unrelated props.

### 8. Dominant-focus dilution

Example: the requested giant tomato is present, but a plush figure, sign, and broccoli cluster remain equally large and colorful.

Cause: source preservation was confused with equal visual priority.

Repair: keep only 0–2 supporting scene cues and demote them in scale, contrast, saturation, and placement.

### 9. Wrong “largest element” selection

Example: a wall or table becomes the Fidelity focus because it occupies more pixels than the product.

Cause: literal image area was used instead of semantic relevance.

Repair: choose the largest meaningful subject element.

### 10. Multi-case blending

Example: three source photos intended for three posters are combined into one generated collage.

Cause: separate cases were not isolated.

Repair: process one source image per generation unless a comparison board is explicitly requested.

## Review questions

After each test, ask:

1. Is the photographed product still unmistakably the same object?
2. Is the product still the visual hero?
3. If Fidelity Mode is active, what is the single selected focus?
4. Is that focus visible before secondary details at thumbnail size?
5. Are the workers one fixed faceless system rather than characters?
6. Can each worker action be traced back to a product feature?
7. Is the empty space doing compositional work?
8. If text exists, does it feel written rather than typeset?
9. What is the single biggest defect to repair next?

## Regression policy

A failure that is likely to repeat should become an eval case in `evals/evals.json`.

Do not rewrite the Skill only around one pretty example. Maintain a small set of different subjects so improvements to one axis do not silently damage another.