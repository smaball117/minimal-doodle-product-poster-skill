---
name: minimal-doodle-product-poster-skill
description: Turn a clear uploaded product or food photo into a minimalist white-space poster with one preserved photographic hero subject, mandatory caption rendering when provided, small faceless doodle workers, product-related micro-storytelling, and loose thin-line Chinese handwriting.
---

# Minimal Doodle Product Poster Skill

Skill revision: **v0.7-worker-scale-calibration**

## Purpose

Turn one real product, food, drink, dessert, fruit, or everyday object into a calm minimalist poster built from:

- one photoreal hero subject;
- large white negative space;
- 3–5 tiny faceless black-line workers;
- short loose handwritten Chinese caption when provided;
- sparse action-serving doodles.

The target is **real product photography + a tiny primitive doodle micro-world**. The workers must remain secondary marks, never co-equal characters.

## Execution priority

1. Subject identity
2. One clear hero subject
3. Caption when provided
4. Worker visual system
5. Worker scale relative to hero
6. Product-related worker actions
7. White-space composition
8. Sparse decorative doodles

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
→ assemble prompt with hard worker/scale rules inlined
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
- loose spacing, slightly uneven size and tilt;
- simple curved hand-drawn arrow may connect caption to subject;
- no extra copy, pinyin, English, labels, badges, or formal typography.

Missing or replaced caption is a failure.

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

**Do not use the previous squat/chubby calibration.**

Target geometry:

- total figure height: approximately **2.8–3.5 head diameters**;
- head: approximately **28%–35% of total figure height**;
- head is visibly larger than torso width, but not giant;
- torso is short and lightly rounded, **not wide or barrel-shaped**;
- torso width is about **55%–75% of head diameter**;
- arms and legs are **slim, simple, and short-to-medium**, not thick/stubby and not long stick limbs;
- almost no visible neck;
- overall silhouette feels light, naive, compact, and slightly clumsy rather than cute/chibi.

Reject:

- oversized chibi heads;
- fat or barrel-shaped bodies;
- thick stubby limbs;
- tall adult stick figures;
- long thin fashion-illustration limbs;
- realistic anatomy.

## Worker scale lock relative to hero

This is a hard composition rule.

- normal worker visual height: approximately **12%–18% of hero subject height**;
- preferred average: around **14%–16%**;
- no worker should exceed **20% of hero subject height** unless the user explicitly requests a close-up worker;
- workers on or behind the product may be partially occluded and can appear smaller;
- the product must visually dominate before any worker is noticed.

If a worker feels almost as important as the product, it is too large.

## Worker action contract

Use 3–5 workers. Each worker must reveal a real product feature.

```text
product feature → physical metaphor → worker action
```

Prefer:

- hold
- carry
- push
- pull
- wipe
- scoop
- arrange
- collect
- inspect
- taste
- clean
- cool
- fan
- rest
- shade

Use selectively:

- pour
- water
- measure
- repair

Do not add a worker only to fill space.

## Structural prop rule

Structural props are **not banned**, but they are low-frequency.

Default structural-prop budget: **0**.
Maximum per poster: **1**.

A ladder/stool/platform may appear only when vertical access genuinely improves the product story.

If used:

- base must visibly rest on the ground plane;
- perspective must match the product;
- top must visibly contact a stable surface or product edge when appropriate;
- worker feet/hands must physically connect;
- it cannot float or terminate in empty space.

Never use a ladder merely because the product is tall. Prefer direct-contact actions first.

Ropes, scaffolds, suspended lines, and floating platforms remain disallowed unless explicitly requested.

## Composition contract

- pure white or very lightly warm-white background;
- normally 70%–80% negative space;
- one photographic hero subject center-lower or slightly off-center;
- caption lives in left whitespace;
- doodles remain sparse;
- workers do not evenly surround the object like a decorative border.

## Photography-first rule

The hero remains realistic photography:

- preserve real texture/material;
- soft high-key studio light;
- realistic highlights and contact shadow;
- no cartoon conversion of the product.

## Quick Mode

One-pass complete poster.

Must still obey:

- Subject Lock;
- mandatory caption when provided;
- worker identity lock;
- worker proportion lock;
- worker scale lock;
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

For `subject_identity` and `dominant_element`, use `prompts/poster-base.md`, then lettering if needed.

## Final prompt assembly requirement

The final generation prompt must explicitly include:

1. hero subject description;
2. exact caption if provided;
3. worker identity lock;
4. worker geometry: 2.8–3.5 heads tall, narrower torso, slim short-to-medium limbs;
5. worker scale: 12%–18% of hero height, max 20%;
6. 3–5 product-related actions;
7. structural-prop budget 0 by default, max 1 grounded ladder/stool if truly useful;
8. large white-space composition;
9. photography-first rule.

Do not rely on vague phrases such as “tiny cute workers”.

## Post-generation self-check

Reject or repair if:

- subject identity drifted;
- multiple photographic objects compete as heroes;
- provided caption is missing/wrong;
- workers have faces, clothes, or mascot styling;
- workers are chubby/chibi with giant heads;
- workers are long-limbed stick figures;
- any worker exceeds 20% of hero height without explicit reason;
- workers visually compete with the hero;
- more than one structural access prop appears;
- a ladder/stool/platform floats or lacks grounding;
- worker actions do not explain product features;
- white space no longer dominates.

## Repair priority

1. caption
2. subject identity
3. worker scale relative to hero
4. worker silhouette/proportion
5. structural-prop grounding/frequency
6. clutter and hierarchy

Use one targeted repair pass.

## Minimal generation skeleton

```text
Generate a minimalist white-background product poster.

Hero:
[exact photoreal subject]

Caption:
Render exactly “[caption]” in thin, loose, naive black Chinese handwriting in the left negative space. Caption is mandatory when provided.

Workers:
Add 3–5 very small primitive faceless black-line workers.
Blank round heads, no face, no hair, no clothing, white interiors, thin uneven black outlines.
Each figure is about 2.8–3.5 heads tall with a lightly rounded narrow torso and slim short-to-medium limbs.
Do not make them chubby/chibi or long-limbed stick figures.
Each worker should normally be only 12%–18% of the hero subject height and never over 20% unless explicitly requested.

Actions:
Each worker performs a distinct action tied to a real product feature.

Props:
Default structural-prop count is zero. At most one grounded ladder/stool may appear only if vertical access genuinely improves the story. No floating ladder, rope, scaffold, suspended line, or platform.

Composition:
Pure white field, large negative space, one hero subject, workers visually secondary.

Style:
Photoreal product + primitive hand-drawn micro-world. Calm, restrained, clean, lightly humorous.
```

## Success definition

A correct result has:

- one unmistakable photographic hero;
- mandatory caption when supplied;
- small faceless workers that feel light and primitive, not fat/chibi and not stick-like;
- workers clearly smaller than the hero;
- meaningful actions;
- grounded, rare structural props;
- generous white space.