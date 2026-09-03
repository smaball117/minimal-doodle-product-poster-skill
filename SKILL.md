---
name: minimal-doodle-product-poster-skill
description: Turn a clear uploaded product or food photo into a minimalist white-space poster with one preserved photographic hero subject, small faceless doodle workers, product-related micro-storytelling, and loose semantic-cluster thin-line Chinese handwriting.
---

# Minimal Doodle Product Poster Skill

Skill revision: **v0.9-semantic-cluster-lettering**

## Purpose

Turn one real product, food, drink, dessert, fruit, or everyday object into a calm minimalist poster built from:

- one photoreal hero subject;
- large white negative space;
- 3–5 tiny faceless black-line workers;
- short loose handwritten Chinese caption when provided;
- sparse action-serving doodles.

The target is **real product photography + a tiny primitive doodle micro-world**. Workers remain secondary marks. Lettering must feel like a handwritten note block, not typeset text and not isolated floating stickers.

## Execution priority

1. Subject identity
2. One clear hero subject
3. Exact caption when provided
4. Caption semantic grouping and spatial rhythm
5. Worker visual system
6. Worker scale relative to hero
7. Product-related worker actions
8. White-space composition
9. Sparse decorative doodles

Higher priority wins when rules conflict.

## Required references

Apply:

- `references/style-guide.md`
- `references/subject-fidelity.md`
- `references/micro-worker-guide.md`
- `references/lettering-guide.md`
- `references/fidelity-focus.md`
- `references/evaluation.md`

Critical rules must also be inlined into the final image-generation prompt.

## Core workflow

```text
input photo
→ identify hero subject
→ Subject Lock
→ optional Scene Lock
→ extract 2–4 real product features
→ convert features into 3–5 worker actions
→ choose Quick or Fidelity
→ if caption exists, split it into natural semantic clusters
→ place clusters as one compact handwritten title block
→ assemble final prompt with hard worker/scale/lettering rules inlined
→ generate
→ self-check
→ one targeted repair if needed
```

## Subject Lock

Preserve the real object category, silhouette, material, main color, defining parts, and necessary support/container relation.

Default composition:

- one hero subject only;
- 0–2 secondary photographic supporting objects;
- secondary objects must be smaller and weaker;
- do not turn a single product into a multi-product collage.

## Caption contract

If the user provides a caption, it is mandatory.

- use the exact requested wording;
- place in upper-left or left negative space;
- thin black naive Chinese handwriting;
- no extra copy, pinyin, English, labels, badges, or formal typography;
- one loose curved hand-drawn arrow may connect the title block to the subject.

Missing, replaced, or mistranslated caption is a failure.

## Semantic Cluster Lettering Lock

The caption must remain a **coherent handwritten phrase**, not a typeset line and not a set of isolated single-character stickers.

### Core rule

**Group by meaning first, then loosen the placement inside and between groups.**

Examples:

- `心态放苹` → `心态` / `放苹`
- `焦糖脑袋冲啊` → `焦糖` / `脑袋` / `冲啊`
- `清甜下午茶` → `清甜` / `下午茶` or another natural semantic grouping

Do not mechanically split every character.

### Cluster spacing rules

- characters inside the same semantic cluster stay relatively close;
- within-cluster spacing may vary, but the characters must still read as one small phrase unit;
- gaps between clusters should usually be about **1.4–2.2×** the typical within-cluster gap;
- clusters may shift up/down and left/right independently;
- clusters do not share one perfect baseline;
- the whole title remains compact in one upper-left / left-side zone;
- avoid long diagonal staircase arrangements that drag across the canvas;
- avoid one-character-per-row layouts unless the user explicitly asks for that style.

### Compact title-block rule

For 4–6 Chinese characters, the title should normally occupy a compact handwritten zone rather than a long path:

- roughly **20%–35% of canvas width**;
- roughly **15%–28% of canvas height**;
- keep clear breathing space around the title block;
- the arrow should originate from the title block as a whole, usually from its lower or side edge.

These are guidance ranges, not rigid geometry, but the title must not span half the poster as a diagonal chain of isolated characters.

### Caption-length routing

- **2 chars**: one loose cluster; slight size, tilt, and baseline mismatch.
- **3 chars**: one cluster or 2+1 grouping; compact, not a long straight line.
- **4 chars**: default to **2 semantic clusters** when natural; loose two-level arrangement; never a perfect 2×2 grid.
- **5–6 chars**: default to **2–3 semantic clusters**; group members stay close; do not scatter all characters independently; do not render as one continuous typeset line.
- **7+ chars**: split into natural semantic groups of roughly 2–3 characters, keeping the overall title block compact and readable.

The goal is: **handwritten phrase structure with imperfect spacing**, not phrase-level typography and not character-level fragmentation.

## Micro-worker identity lock

Every worker belongs to one fixed primitive character system:

- blank round or slightly irregular head;
- no eyes, nose, mouth, eyebrows, or expression;
- no hair, hat, clothing details, labels, logos, or body symbols;
- white empty interior;
- thin uneven black single-line outline;
- simple rounded torso;
- simplified hands and feet;
- no polished mascot finish.

## Worker proportion lock

Target geometry:

- total figure height: approximately **2.8–3.5 head diameters**;
- head: approximately **28%–35% of total figure height**;
- head larger than torso width, but not giant;
- torso short and lightly rounded, not wide or barrel-shaped;
- torso width about **55%–75% of head diameter**;
- arms and legs slim, simple, and short-to-medium;
- almost no visible neck;
- overall silhouette light, naive, compact, slightly clumsy rather than cute/chibi.

Reject giant chibi heads, fat/barrel bodies, thick stubby limbs, tall adult stick figures, long fashion limbs, and realistic anatomy.

## Worker scale lock relative to hero

- normal worker visual height: approximately **12%–18% of hero subject height**;
- preferred average: about **14%–16%**;
- no worker over **20%** of hero height unless explicitly requested;
- product must be noticed before any worker.

If a worker feels almost as important as the product, it is too large.

## Worker action contract

Use 3–5 workers. Each worker must reveal a real product feature.

```text
product feature → physical metaphor → worker action
```

Prefer hold, carry, push, pull, wipe, scoop, arrange, collect, inspect, taste, clean, cool, fan, rest, shade.

Use pour, water, measure, repair selectively.

Do not add a worker only to fill space.

## Structural prop rule

Structural props are low-frequency.

- default structural-prop budget: **0**;
- maximum per poster: **1**;
- ladder/stool/step only when vertical access genuinely improves the story;
- base must rest on the ground plane;
- perspective must match;
- top/contact must be physically believable;
- worker feet/hands must connect;
- never use a ladder merely because the product is tall.

Ropes, scaffolds, suspended lines, and floating platforms remain disallowed unless explicitly requested.

## Composition contract

- pure white or very lightly warm-white background;
- normally 70%–80% negative space;
- one photographic hero subject center-lower or slightly off-center;
- caption lives in left whitespace as one compact handwritten block;
- doodles remain sparse;
- workers do not evenly surround the object like a decorative border.

## Photography-first rule

The hero remains realistic photography with real texture/material, soft high-key studio light, realistic highlights, and contact shadow. Do not cartoonize the product.

## Quick Mode

One-pass complete poster.

Must still obey:

- Subject Lock;
- mandatory caption;
- Semantic Cluster Lettering Lock;
- worker identity/proportion/scale locks;
- structural-prop budget;
- white-space layout;
- photography-first rule.

## Fidelity Mode

```yaml
mode: fidelity
fidelity_focus: subject_identity | dominant_element | lettering
```

Only one focus per pass.

- `subject_identity`: restore category, silhouette, material, defining details.
- `dominant_element`: make the largest meaningful subject feature the first photographic signal.
- `lettering`: freeze accepted poster base and repair only the title layer.

For `subject_identity` and `dominant_element`, use `prompts/poster-base.md`, then `prompts/lettering-layer.md` if lettering is required.

If glyphs are correct but the layout feels either too typeset or too fragmented, use `fidelity_focus: lettering` and repair semantic clustering + spacing only.

## Final prompt assembly requirement

The final generation prompt must explicitly include:

1. hero subject description;
2. exact caption if provided;
3. natural semantic cluster plan for the caption;
4. compact title-block rule;
5. within-cluster vs between-cluster spacing rule;
6. worker identity lock;
7. worker geometry: 2.8–3.5 heads tall, narrower torso, slim short-to-medium limbs;
8. worker scale: 12%–18% of hero height, max 20%;
9. 3–5 product-related actions;
10. structural-prop budget 0 by default, max 1 grounded ladder/stool if truly useful;
11. large white-space composition;
12. photography-first rule.

Do not rely on vague phrases such as “handwritten text” or “tiny cute workers”.

## Post-generation self-check

Reject or repair if:

- subject identity drifted;
- multiple photographic objects compete as heroes;
- provided caption is missing/wrong;
- 5+ character caption is rendered as one neat continuous typeset line;
- every character is isolated with no visible phrase grouping;
- a 5–6 character title forms a long diagonal staircase across the canvas;
- 4-character caption forms a perfect 2×2 grid;
- title block spreads too far and competes with the product;
- workers have faces, clothes, or mascot styling;
- workers are chubby/chibi or long-limbed stick figures;
- any worker exceeds 20% of hero height without explicit reason;
- workers visually compete with hero;
- more than one structural access prop appears;
- ladder/stool/platform floats or lacks grounding;
- worker actions do not explain product features;
- white space no longer dominates.

## Repair priority

1. caption correctness
2. caption semantic clustering
3. caption compactness and spacing rhythm
4. subject identity
5. worker scale relative to hero
6. worker silhouette/proportion
7. structural-prop grounding/frequency
8. clutter and hierarchy

Use one targeted repair pass.

## Minimal generation skeleton

```text
Generate a minimalist white-background product poster.

Hero:
[exact photoreal subject]

Caption:
Render exactly “[caption]”. Caption is mandatory when provided.
First split the caption into natural semantic clusters, for example [cluster 1] / [cluster 2] / [cluster 3].
Keep characters inside each cluster relatively close so they read as a phrase unit. Make gaps between clusters clearly larger than within-cluster gaps. Let clusters drift slightly in x/y position and baseline, but keep the whole title compact in the upper-left/left whitespace.
Do not typeset the whole sentence as one clean line. Do not scatter every character as an isolated sticker. Do not create a long diagonal staircase.
Use thin naive black handwriting with subtle variation in size, tilt, and glyph skeleton.

Workers:
Add 3–5 very small primitive faceless black-line workers.
Blank round heads, no face, no hair, no clothing, white interiors, thin uneven black outlines.
Each figure is about 2.8–3.5 heads tall with a lightly rounded narrow torso and slim short-to-medium limbs.
Each worker should normally be only 12%–18% of hero height and never over 20% unless explicitly requested.

Actions:
Each worker performs a distinct action tied to a real product feature.

Props:
Default structural-prop count is zero. At most one grounded ladder/stool may appear only if vertical access genuinely improves the story.

Composition:
Pure white field, large negative space, one hero subject, workers visually secondary.

Style:
Photoreal product + primitive hand-drawn micro-world. Calm, restrained, clean, lightly humorous.
```

## Success definition

A correct result has:

- one unmistakable photographic hero;
- mandatory caption when supplied;
- handwritten glyphs grouped into natural semantic clusters;
- group members close enough to read as phrases;
- cluster spacing loose enough to feel handwritten;
- compact title block rather than one neat line or isolated-character staircase;
- small faceless workers that feel light and primitive;
- workers clearly smaller than hero;
- meaningful actions;
- rare grounded structural props;
- generous white space.