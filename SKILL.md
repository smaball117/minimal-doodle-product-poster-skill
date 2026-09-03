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
+ 4–5 expressionless round-headed miniature workers
+ one short loose handwritten caption
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
reference_image: optional
```

If a reference image is provided, source fidelity has priority over invention. First identify the exact object category, form, color, toppings, surface material, and silhouette. Do not reinterpret one food type as another merely because their colors are similar.

Example: a molded blue pudding must remain a molded blue pudding. It must not become shaved ice, a cake, a jelly mountain, or another dessert form.

When analyzing a reference, extract:

1. exact subject identity and category;
2. subject shape, proportions, color, toppings, and surface texture;
3. negative-space ratio;
4. hero-subject placement and scale;
5. subject realism and lighting;
6. doodle line quality;
7. relationship between doodles and product;
8. caption position and tone;
9. palette restrictions.

Do not merely enumerate visible objects. Explain why the composition works.

## Reasoning workflow

### Step 1 — Lock subject identity first

Before generating ideas, determine what the photographed object actually is.

Preserve:

- product category;
- primary silhouette;
- main color;
- surface material;
- visible topping and garnish;
- plate/container relationship when visually important.

Ignore unrelated background props unless the user explicitly wants them retained.

Never change the product category for the sake of a stronger visual metaphor.

### Step 2 — Extract product features

Identify 2–4 features that can become physical actions.

Examples:

- watermelon → juicy, hydrating, chilled, seeded;
- peach → sweet, soft, ripe, fuzzy skin;
- lemon soda → fizzy, icy, sour-fresh, refreshing;
- blue pudding → cool, smooth, soft, jiggly, creamy;
- ice cube → cool, melting, transparent, restful.

Prefer visible, tactile, or emotional features. Avoid generic marketing adjectives that cannot be visualized.

### Step 3 — Convert features into miniature jobs

Create 4–5 different worker actions. Every action must have a direct relationship with the subject.

Good pattern:

```text
feature → metaphor → worker action
hydrating → water supply → worker uses a hose
seeds → cargo → worker transports seeds in a cart
sweetness → quality inspection → worker measures sweetness
cooling → climate control → worker operates a fan
soft texture → tasting/testing → worker uses a tiny spoon
```

Bad pattern:

```text
random person waving
random stars
random decorative character
unrelated balloons
```

At least 3 actions should clearly communicate a product feature without needing explanatory text.

### Step 4 — Build composition

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

### Step 5 — Control photography

The hero subject must look like premium commercial photography:

- realistic materials and surface texture;
- clean studio soft light;
- soft contact shadow;
- bright high-key exposure;
- natural translucency, moisture, bubbles, fruit flesh, cream, pudding gloss, glass, or ice detail when relevant;
- no complex environmental background.

If a source photo is provided, preserve its object identity and recognizable form while simplifying the surrounding scene into the poster system.

The subject must not become an illustration, sticker, clay render, toy, or 3D cartoon.

### Step 6 — Control doodle characters

The miniature people are a fixed character system, not individually designed characters.

Character rules:

- black single-line drawing only;
- round blank head;
- no eyes, mouth, nose, eyebrows, or facial expression;
- no hairstyle;
- no hats;
- no clothing details;
- no uniforms;
- no logos, labels, text, badges, or decorative symbols on the body;
- simple neutral body silhouette;
- intentionally naive anatomy;
- slightly uneven hand-drawn contour;
- no filled color areas;
- no polished vector aesthetic;
- no manga rendering;
- no detailed character design.

The pose and job tool should communicate the action. Emotion must come from body posture and the situation, not from facial expressions or costumes.

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

### Step 7 — Write the caption and handwriting

Caption content rules:

- preferably 2–6 Chinese characters;
- conversational rather than slogan-like;
- slightly playful, calm, observational, or product-inspired;
- may use light wordplay or gentle homophones when natural;
- tied to the subject's strongest feature;
- keep wording short to reduce text-generation errors;
- text participates in the composition and does not have to behave like a formal title.

Handwriting rules:

- thin black handwritten strokes;
- naive, loose, slightly awkward structure;
- not a standard printed font;
- not calligraphy;
- not rounded cute typography;
- not neat typesetting;
- characters may tilt slightly;
- character sizes may vary;
- horizontal strokes may extend unusually long;
- spacing and internal structure may feel loose and irregular;
- preserve legibility while allowing obvious human imperfection.

Typical placement is upper-left or left-side negative space, often with a loose hand-drawn arrow pointing toward the subject.

Examples of tone:

- 补水中
- 今天有点甜
- 请勿打扰
- 正在降温
- 清甜下午茶

Avoid long copy, feature lists, pricing text, logo systems, and dense typography.

### Step 8 — Restrict color

Default rule: use only colors already present in the photographed subject plus white background and black doodle lines.

Do not introduce unrelated accent colors unless the user explicitly requests them.

### Step 9 — Output the prompt in exactly three sections

Preserve the user's preferred three-step structure.

#### 1. Base visual and composition

Describe:

- minimalist healing poster;
- premium product-photography feeling;
- pure white background;
- negative-space ratio;
- one realistic hero subject;
- source-image fidelity if a reference is supplied;
- studio soft light;
- black hand-drawn miniature world;
- purposeful worker interactions.

#### 2. Style controls and exclusions

Describe the overall restraint, handwriting style, fixed doodle-character system, color logic, and important exclusions.

Prefer positive instructions first. Keep exclusions concise and functional.

#### 3. Subject-specific scene

Describe:

- the exact subject identity and photographic details;
- 4–5 worker actions;
- handwritten caption;
- arrow placement;
- final palette.

## Output quality checklist

Before answering, verify:

- [ ] If a reference exists, is the product category preserved exactly?
- [ ] Are the source object's shape, main color, toppings, and material recognizable?
- [ ] Is there only one hero subject?
- [ ] Does the image retain 70%–80% breathing room?
- [ ] Is the subject explicitly realistic photography?
- [ ] Are doodles black, simple, and hand-drawn rather than polished illustration?
- [ ] Are all miniature people round-headed, blank-faced, and free of clothing/labels?
- [ ] Does every miniature worker have a product-related job?
- [ ] Are the worker actions different from one another?
- [ ] Is the caption short and linked to a core feature?
- [ ] Does the lettering look loose, thin, irregular, and handwritten rather than typeset?
- [ ] Is the palette restricted to the product colors + white + black?
- [ ] Are logos, borders, dense layout, 3D cartoons, anime, and colored illustration excluded?
- [ ] Is the final prompt organized into exactly three sections?

## Failure modes and corrections

### Wrong product identity

Example: pudding becomes shaved ice.

Correction: explicitly lock the source category, silhouette, material, topping, and plate/container before describing style. Remove metaphors that alter the physical object.

### Too much decoration

Correction: remove half the doodles and restore white space.

### Looks like a children's illustration

Correction: strengthen realistic studio photography and reduce character detail.

### Character design is too specific

Example: workers gain hats, uniforms, faces, labels, or cute expressions.

Correction: return to a blank round head, expressionless face, simple unclothed line body, and communicate actions only through pose and tools.

### Miniature people feel random

Correction: rewrite each action from a specific product feature.

### Handwriting looks like a font

Correction: specify thin black hand strokes, uneven character size, loose structure, mild tilt, irregular spacing, and occasional elongated horizontal strokes. Remove requests for “cute font”, calligraphy, or clean typography.

### Subject looks synthetic or plastic

Correction: add material-specific photographic detail such as condensation, pulp fibers, bubbles, transparency, pudding gloss, cream texture, soft fuzz, or natural surface imperfections.

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