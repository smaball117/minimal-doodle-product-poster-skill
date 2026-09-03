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

For complex scenes, also identify 1–3 **Scene Lock** cues that make the source recognizable. Do not preserve every background object.

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

Use **Fidelity Mode** when the user wants one accepted visual property to be protected or emphasized.

#### Quick Mode

Read `prompts/quick-prompt.md` and generate subject + workers + text in one pass.

Quick Mode is best for:

- first exploration;
- fast concept testing;
- simpler source photos;
- testing whether the visual language works at all.

#### Fidelity Mode

Read `references/fidelity-focus.md` first.

Choose exactly one primary focus:

```yaml
mode: fidelity
fidelity_focus: subject_identity | dominant_element | lettering
```

Routing:

- exact subject preservation → `subject_identity`
- emphasize the largest / strongest / named element → `dominant_element`
- repair only Chinese handwriting → `lettering`

For `subject_identity` or `dominant_element`:

1. read `prompts/poster-base.md`;
2. create a no-title poster base using the chosen fidelity focus;
3. if text is required, read `references/lettering-guide.md` and `prompts/lettering-layer.md`;
4. composite the accepted title onto the accepted poster base when tooling allows.

For `lettering`:

1. freeze the accepted poster base;
2. do not regenerate the product, workers, lighting, or composition;
3. read `references/lettering-guide.md`;
4. regenerate only the title layer;
5. composite it back onto the unchanged base.

One Fidelity pass should solve one main fidelity problem. If several problems remain, solve them sequentially rather than redesigning everything at once.

### 5. Dominant-element behavior

When `fidelity_focus: dominant_element`:

- identify the largest **meaningful** source element, not irrelevant background architecture;
- make that focus the first photographic signal;
- normally scale it to roughly 45%–60% of canvas height depending on shape;
- allow roughly 60%–70% negative space if needed for stronger emphasis;
- keep only 0–2 photographic supporting cues;
- make workers interact with the focus element first;
- keep all secondary elements clearly weaker in size, contrast, saturation, and placement.

Examples already validated in tests:

```text
vegetable farm → giant red tomato
seafood soup → central yellow character-shaped ingredient
caramel ice cream → large caramel biscuit
apple tea → red apple / apple slices when “苹” is the semantic hook
```

### 6. Lettering rules

If the poster contains Chinese text, read `references/lettering-guide.md`.

The target lettering is thin black, naive, loose, slightly awkward, irregular, and readable. It is not standard typography, calligraphy, rounded cute handwriting, or polished commercial lettering.

### 7. Evaluate before finalizing

Read `references/evaluation.md` and check the result against both the global criteria and the selected fidelity focus.

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

## Lock hierarchy

Use three separate locks:

```text
Subject Lock = what is it?
Scene Lock = what source cues make the scene recognizable?
Focus Lock = what must become the first visual signal in this pass?
```

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

When multiple source images are provided for separate posters, process them as independent cases. Do not intentionally combine them into one collage unless the user asks for a comparison board.

When a test reveals a repeatable failure, add it to `evals/evals.json` in a future repository revision.

## Scope boundary

This skill intentionally stays narrow. It does not include flavor monsters, mascots, desktop pets, character packs, animation runtimes, or general brand systems. Its specialty is one thing done well: **real photographic object + minimal faceless doodle workers + restrained handwritten storytelling**.