---
name: minimal-doodle-product-poster-skill
description: Turn a clear uploaded product or food photo into a minimalist white-space poster with a preserved photographic subject, primitive faceless doodle workers, product-related micro-storytelling, and optional loose thin-line Chinese handwriting.
---

# Minimal Doodle Product Poster Skill

## Purpose

Use this skill for a single real product, food, drink, dessert, fruit, or simple daily object that should become a quiet minimalist poster built from real photography + primitive black doodles.

Do not imitate official brand assets. Do not add logos, mascots, packaging marks, or claims of affiliation unless the user supplies authorized material and explicitly requests it.

## Core routing

### 1. Inspect the input first

If a reference photo exists, resolve the subject before any creative work.

- If there is no clear usable subject, ask for a clearer image.
- If there are several independent possible subjects and the user has not identified one, ask which one to use.
- Treat a container and its contents as one subject unless the user says otherwise.
- Once the subject is identified, lock its category, silhouette, material, main color, topping/garnish, and important support/container relation.

Read `references/subject-fidelity.md`.

### 2. Read the visual system

Read `references/style-guide.md` before writing or generating the poster.

The non-negotiable visual formula is:

```text
large white negative space
+ one preserved photographic hero object
+ primitive black doodle intervention
+ faceless round-headed micro workers
+ product-related actions
+ restrained subject-derived color
```

### 3. Build the micro story

Read `references/micro-worker-guide.md`.

Convert 2–4 real product features into 3–5 physical jobs. Every worker must have one clear action verb and one visible relationship with the product.

Do not add workers merely to fill space.

### 4. Choose generation mode

Use **Quick Mode** by default for exploration.

Use **Fidelity Mode** when:

- the user emphasizes exact subject preservation;
- the user cares strongly about the handwritten Chinese title;
- a previous all-in-one generation changed the object;
- a previous title looked like a normal font;
- the user asks to revise only the title without disturbing the poster.

#### Quick Mode

Read `prompts/quick-prompt.md` and generate subject + workers + text in one pass.

#### Fidelity Mode

1. Read `prompts/poster-base.md` and create the poster without any title.
2. Read `references/lettering-guide.md`.
3. Read `prompts/lettering-layer.md` and create only the title layer.
4. Composite the accepted title onto the unchanged poster base when tooling allows.

Never regenerate the whole poster as the primary fix for a lettering-only problem.

### 5. Lettering rules

If the poster contains Chinese text, read `references/lettering-guide.md`.

The target lettering is thin black, naive, loose, slightly awkward, irregular, and readable. It is not standard typography, calligraphy, rounded cute handwriting, or polished commercial lettering.

### 6. Evaluate before finalizing

Read `references/evaluation.md` and check the result.

A successful poster must preserve:

- exact subject category and recognizable form;
- photographic material realism;
- strong white negative space;
- primitive black-line workers;
- blank round heads with no facial features;
- no clothing, hair, hats, labels, or character branding;
- product-related action storytelling;
- restrained colors;
- loose handwritten text when text is used.

## Fixed figure contract

Every micro worker follows the same fixed system:

- blank round or slightly lumpy head;
- no eyes, mouth, nose, eyebrows, or expression;
- no hairstyle;
- no hats;
- no clothes or uniforms;
- no logo, label, badge, text, or decorative body symbol;
- simple neutral body outline;
- black line only;
- uneven hand-drawn contour;
- action communicated by pose + tool + contact with the product.

This contract has higher priority than decorative creativity.

## Subject lock contract

Creative metaphors may change what workers do, but may not change what the photographed object is.

Bad:

```text
blue pudding → “cool” → shaved ice
```

Good:

```text
blue pudding → “cool / smooth / jiggly” → workers inspect, taste, climb, cool, or maintain the pudding while the pudding remains unchanged
```

## Output behavior

When the user asks for a prompt, provide the generation-ready prompt only unless analysis is requested.

When the user asks to generate an image and image generation is available, use the workflow above rather than merely describing it.

When a test reveals a repeatable failure, add it to `evals/evals.json` in a future repository revision.

## Scope boundary

This skill intentionally stays narrow. It does not include flavor monsters, mascots, desktop pets, character packs, animation runtimes, or general brand systems. Its specialty is one thing done well: **real photographic object + minimal faceless doodle workers + restrained handwritten storytelling**.