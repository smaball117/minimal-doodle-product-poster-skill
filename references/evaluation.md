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
- [ ] White / warm-white negative space remains generous, normally around 70%–80%.
- [ ] The object sits center-lower or another intentionally quiet lower position.
- [ ] Doodles do not evenly fill the blank field.
- [ ] No dense ad-layout clutter appears.

### C. Micro workers

- [ ] Workers use blank round heads.
- [ ] No eyes, mouths, facial expressions, hair, hats, or clothing details appear.
- [ ] No labels, logos, badges, or body symbols appear.
- [ ] Lines are black, simple, uneven, and hand-drawn.
- [ ] Every worker has a clear action verb.
- [ ] Every action relates to a real product feature.
- [ ] At least three workers have readable contact or cause-and-effect with the product.
- [ ] Removing any worker would remove a layer of product meaning.

### D. Lettering

When text is used:

- [ ] Exact requested wording is attempted without extra copy.
- [ ] The lettering uses thin black lines.
- [ ] Character sizes, tilt, spacing, and baselines are irregular.
- [ ] The result does not look like standard computer typography.
- [ ] It is not brush calligraphy, rounded cute handwriting, or polished commercial lettering.
- [ ] Text participates in composition rather than forming a formal ad block.

When typography is the only failure, switch to Fidelity Mode and keep the poster base unchanged.

### E. Palette

- [ ] Colors come from the source subject plus white and black.
- [ ] No unrelated accent color was added without user request.

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

## Review questions

After each test, ask:

1. Is the photographed product still unmistakably the same object?
2. Is the product still the visual hero?
3. Are the workers one fixed faceless system rather than characters?
4. Can each worker action be traced back to a product feature?
5. Is the empty space doing compositional work?
6. If text exists, does it feel written rather than typeset?
7. What is the single biggest defect to repair next?

## Regression policy

A failure that is likely to repeat should become an eval case in `evals/evals.json`.

Do not rewrite the Skill only around one pretty example. Maintain a small set of different subjects so improvements to one axis do not silently damage another.