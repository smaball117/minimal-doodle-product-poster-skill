---
name: minimal-doodle-product-poster-skill
description: Generate minimalist healing product-poster prompts using large white space, realistic product photography, black hand-drawn doodles, miniature worker storytelling, and short handwritten captions.
---

# Minimal Doodle Product Poster Skill

## Purpose

Use this skill when the user wants a minimalist product poster built from:

- large white negative space;
- one realistic photographic product or food subject;
- a small number of black hand-drawn doodles;
- miniature people whose actions explain product features;
- a short handwritten Chinese caption and arrow;
- restrained colors derived from the subject itself.

This style may be casually referred to by users as “喜茶风”. Do not rely on brand imitation language. Reconstruct the visual logic from first principles.

## Core visual formula

```text
Minimal premium product photography
+ 70%–80% white negative space
+ one hero subject placed center-lower
+ loose black marker-like line doodles
+ 4–5 miniature workers with purposeful actions
+ one short handwritten emotional caption
= quiet, healing, playful micro-world product poster
```

## When to use

Use for:

- fruit;
- drinks;
- desserts;
- ice and cooling objects;
- simple summer products;
- single objects with clear physical or emotional features.

Do not default to this skill for:

- dense commercial key visuals;
- multi-product collages;
- complex brand-layout systems;
- 3D cartoon scenes;
- full illustration posters;
- anime or comic art;
- cyberpunk or highly decorative visual systems.

## Input model

The user may provide only a subject. Infer the rest when reasonable.

Preferred variables:

```yaml
subject: required
feature: optional
caption: optional
worker_count: optional, default 4-5
color_palette: optional
aspect_ratio: optional, default vertical poster
```

If a reference image is provided, first analyze only the reusable visual logic:

1. negative-space ratio;
2. hero-subject placement and scale;
3. subject realism and lighting;
4. doodle line quality;
5. relationship between doodles and product;
6. caption position and tone;
7. palette restrictions.

Do not merely enumerate visible objects. Explain why the composition works.

## Reasoning workflow

### Step 1 — Extract product features

Identify 2–4 features that can become physical actions.

Examples:

- watermelon → juicy, hydrating, chilled, seeded;
- peach → sweet, soft, ripe, fuzzy skin;
- lemon soda → fizzy, icy, sour-fresh, refreshing;
- ice cube → cool, melting, transparent, restful.

Prefer visible, tactile, or emotional features. Avoid generic marketing adjectives that cannot be visualized.

### Step 2 — Convert features into miniature jobs

Create 4–5 different worker actions. Every action must have a direct relationship with the subject.

Good pattern:

```text
feature → metaphor → worker action
hydrating → water supply → worker uses a hose
seeds → cargo → worker transports seeds in a cart
sweetness → quality inspection → worker measures sweetness
cooling → climate control → worker operates a fan
```

Bad pattern:

```text
random person waving
random stars
random decorative character
unrelated balloons
```

At least 3 actions should clearly communicate a product feature without needing explanatory text.

### Step 3 — Build composition

Default composition:

- pure white background;
- 70%–80% negative space;
- one hero subject only;
- subject positioned center-lower;
- subject occupies approximately 30%–45% of the canvas height depending on shape;
- handwritten caption on the upper-left or left side;
- one loose arrow linking caption to subject;
- doodles cluster around and interact with the subject instead of filling empty space evenly.

The blank area is structural, not unused space. Do not “fix” it by adding decoration.

### Step 4 — Control photography

The hero subject must look like premium commercial photography:

- realistic materials and surface texture;
- clean studio soft light;
- soft contact shadow;
- bright high-key exposure;
- natural translucency, moisture, bubbles, fruit flesh, glass, or ice detail when relevant;
- no complex environmental background.

The subject must not become an illustration, sticker, clay render, toy, or 3D cartoon.

### Step 5 — Control doodles

Doodle rules:

- black line only;
- thin-to-medium single-line drawing;
- imperfect, spontaneous marker/pen feeling;
- simple rounded miniature people;
- intentionally naive anatomy;
- minimal facial detail or no facial detail;
- no filled color areas;
- no polished vector aesthetic;
- no manga rendering;
- no detailed character design.

Useful doodle vocabulary:

- ladders;
- arrows;
- carts;
- hoses;
- umbrellas;
- fans;
- spoons;
- measuring tools;
- clouds;
- small wave lines;
- motion marks.

Only use tools that make sense for the subject's story.

### Step 6 — Write the caption

Caption rules:

- preferably 2–6 Chinese characters;
- conversational rather than slogan-like;
- slightly playful, calm, or observational;
- visually tied to one key product feature;
- handwritten black text;
- normally placed upper-left or left.

Examples of tone:

- 补水中
- 今天有点甜
- 请勿打扰
- 正在降温
- 清爽营业中

Avoid long copy, feature lists, pricing text, logo systems, and dense typography.

### Step 7 — Restrict color

Default rule: use only colors already present in the photographed subject plus white background and black doodle lines.

Do not introduce unrelated accent colors unless the user explicitly requests them.

### Step 8 — Output the prompt in exactly three sections

Preserve the user's preferred three-step structure.

#### 1. Base visual and composition

Describe:

- minimalist healing poster;
- premium product-photography feeling;
- pure white background;
- negative-space ratio;
- one realistic hero subject;
- studio soft light;
- black hand-drawn miniature world;
- purposeful worker interactions.

#### 2. Style controls and exclusions

Describe the overall restraint, color logic, and important exclusions.

Prefer positive instructions first. Keep exclusions concise and functional.

#### 3. Subject-specific scene

Describe:

- the exact subject and photographic details;
- 4–5 worker actions;
- handwritten caption;
- arrow placement;
- final palette.

## Output quality checklist

Before answering, verify:

- [ ] Is there only one hero subject?
- [ ] Does the image retain 70%–80% breathing room?
- [ ] Is the subject explicitly realistic photography?
- [ ] Are doodles black, simple, and hand-drawn rather than polished illustration?
- [ ] Does every miniature worker have a product-related job?
- [ ] Are the worker actions different from one another?
- [ ] Is the caption short and linked to a core feature?
- [ ] Is the palette restricted to the product colors + white + black?
- [ ] Are logos, borders, dense layout, 3D cartoons, anime, and colored illustration excluded?
- [ ] Is the final prompt organized into exactly three sections?

## Failure modes and corrections

### Too much decoration

Correction: remove half the doodles and restore white space.

### Looks like a children's illustration

Correction: strengthen realistic studio photography and reduce character detail.

### Miniature people feel random

Correction: rewrite each action from a specific product feature.

### Subject looks synthetic or plastic

Correction: add material-specific photographic detail such as condensation, pulp fibers, bubbles, transparency, soft fuzz, or natural surface imperfections.

### Poster feels like a normal ad layout

Correction: remove secondary copy, grids, badges, pricing, logo, frames, and decorative typography.

### Too many colors

Correction: return to subject-derived colors only.

## Default response format

When the user asks for a prompt, output only what is needed to generate the image unless they explicitly ask for analysis.

Use:

```text
1、[Base visual and composition prompt]

2、[Style controls and exclusions]

3、[Subject-specific scene prompt]
```

Keep the language concrete, visual, and directly usable by an image-generation model.