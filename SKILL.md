---
name: minimal-doodle-product-poster-skill
description: Turn a clear uploaded product or food photo into a minimalist white-space poster with one preserved photographic hero subject, mandatory caption rendering when provided, primitive faceless doodle workers, product-related micro-storytelling, and loose thin-line Chinese handwriting.
---

# SKILL.md

## Purpose

This skill turns a real photo of a product, food, drink, or everyday object into a **minimal white-background poster** with:

- **one locked photoreal hero subject**
- **large breathing whitespace**
- **3–5 tiny black line micro-workers**
- **short handwritten Chinese caption**
- **light doodle elements such as arrow / cloud / wave line**

The visual goal is calm, clean, healing, minimal, and story-driven.

This skill must prioritize **execution stability** over expressive freedom.

---

## Execution Priority

Always follow this priority order:

1. **Subject identity**
2. **Single hero subject composition**
3. **Caption rendering**
4. **Micro-worker figure system**
5. **Product-related worker actions**
6. **Whitespace layout**
7. **Sparse doodle decoration**

If anything conflicts, **higher priority wins**.

---

## Required Reference Loading

Before generating, the assistant must actively apply the rules from these files:

- `references/style-guide.md`
- `references/subject-fidelity.md`
- `references/micro-worker-guide.md`
- `references/lettering-guide.md`
- `references/fidelity-focus.md`
- `references/evaluation.md`

However, the final generation prompt must **not rely on these files being read indirectly**. The most important rules must be **inlined into the final prompt**.

---

## Core Execution Workflow

```text
Input photo
→ identify hero subject
→ build Subject Lock
→ if scene is complex, build Scene Lock
→ extract 2–4 real product features
→ convert features into 3–5 worker actions
→ choose Quick Mode or Fidelity Mode
→ if Fidelity, choose exactly one fidelity_focus
→ assemble final prompt with hard constraints inlined
→ generate
→ self-check
→ if failed, repair once according to repair priority
```

---

## 1. Subject Lock

Before any generation, identify the real product or object the poster is about.

### Rules

- There must be **one clear hero subject**.
- Supporting props may exist, but must remain **visually secondary**.
- Do **not** change the product category.
- Do **not** replace the original object with a conceptually similar but different object.
- Do **not** expand one product into a multi-product collage unless the user explicitly asks for it.
- If the input image is complex, simplify it while preserving the most important product identity clues.

### Subject Lock Output

Summarize internally like this before prompt assembly:

```yaml
subject_identity:
  category: [what it is]
  silhouette: [main shape]
  material: [surface / realism cues]
  key_parts:
    - [...]
    - [...]
```

### Failure Examples

- blue pudding becomes shaved ice
- apple tea becomes generic orange drink
- one hero drink becomes lip gloss + dessert multi-hero display

---

## 2. Hero Subject Count

Default rule:

- **1 hero subject only**

Supporting items:

- maximum **2** supporting objects
- they must be **smaller**, **weaker**, and **compositionally secondary**
- they must not compete with the hero subject

If the image starts to feel like a commercial product collage, simplify it.

---

## 3. Scene Lock

Use Scene Lock only when the original photo contains meaningful context that helps recognition.

### Rules

- Preserve only **1–3** scene clues.
- Keep them reduced and secondary.
- Scene clues must not overwhelm the white-background poster structure.

### Examples

- apple tea: one or two real apples may remain as scene support
- vegetable farm installation: a small amount of broccoli or signage may remain as support
- soup bowl: bowl shape and one key side ingredient may remain as support

---

## 4. Caption Contract (Mandatory)

If the user provides a caption, **caption rendering is mandatory**.

### Rules

- Render the **exact caption text**.
- Place it in the **upper-left** or **left-side whitespace area**.
- Use **thin black handwritten Chinese**.
- Pair it with a **simple hand-drawn arrow** pointing to the hero subject.
- Keep the caption short.
- The caption must feel like part of the image, not formal typesetting.

### Caption Style

- naive
- loose
- thin black line
- uneven sizing
- slightly crooked
- relaxed spacing
- not a standard digital font

### Failure Conditions

The result is a failure if any of these happen:

- caption missing
- caption replaced with different text
- caption rendered as standard computer font
- caption becomes formal typography
- caption placed far away from the left whitespace structure

### Important Rule

If the user supplies a Chinese caption, **never omit the title**.

---

## 5. Locked Micro-Worker Figure System

Micro-workers are strictly locked.

### Required figure design

- oversized round blank head
- no eyes
- no nose
- no mouth
- no eyebrows
- no facial expression
- no hair
- no hat
- no clothing details
- no accessories
- no labels
- white empty interior
- thin black uneven single-line outline only
- short compact rounded torso
- short stubby arms
- short stubby legs
- almost no visible neck
- tiny rounded hand and foot ends

### Worker Silhouette Lock

The body shape is non-negotiable.

Required proportions:

- total figure height: approximately **2.2–2.8 head diameters**
- head occupies about **35%–45% of total figure height**
- body feels squat, soft, primitive, and slightly clumsy
- arms and legs stay short and compact

Do **not** generate:

- stick figures
- long thin arms
- long thin legs
- realistic adult anatomy
- fashion-illustration proportions
- 4–6 head-tall characters
- polished cartoon mascots

### Prohibited figure drift

Do **not** let workers become:

- mascots
- cute characters
- polished cartoon figures
- decorative illustration people
- dressed-up figures
- expressive emoji-like characters

The workers must remain **quiet, squat, minimal, faceless, and secondary**.

---

## 6. Worker Action Contract

Workers are not random decoration.

### Rules

- use **3 to 5** workers
- each worker must perform a **different** action
- each action must explain one real product feature
- workers must physically or narratively interact with the subject
- choose the **action first**, then add the smallest necessary prop
- if an action does not help explain the product, remove it

### Preferred action pool

Prefer direct-contact actions:

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

Disabled by default:

- climb
- ladder
- rope
- scaffold
- platform

### Action Logic

Use this conversion:

```text
product feature
→ action metaphor
→ worker task
```

### Examples

**Apple tea**
- apple slices → carry or place apple slice
- garnish → inspect or adjust garnish by direct touch
- chilled drink → move ice / cool drink
- fresh serving feel → clean spill / tidy serving area

**Pudding**
- smooth surface → polish surface
- whipped cream → adjust topping
- cherry → inspect or steady the topping from the product edge; do not default to a ladder

**Watermelon**
- watery / juicy → water or tend the fruit
- seeds → collect or move seeds
- cool summer feel → sit in shade / scoop watermelon

### Structural Prop Rule

Ladders, stairs, scaffolds, ropes, platforms, and similar structural props are **forbidden by default**.

Do not use a ladder unless:

1. the user explicitly asks for one; or
2. the concept cannot be communicated clearly without vertical access.

Every physical prop must obey real spatial grounding:

- it must have visible support
- its base must rest on the same ground plane as the product
- it must obey scene perspective
- it cannot float
- it cannot terminate in empty space
- if leaning, it must visibly contact a real surface
- the worker's hands or feet must visibly connect to it

If spatial grounding is unclear, **remove the prop**.

---

## 7. Composition Contract

The layout must follow this formula:

- pure white or near-white background
- **70%–80% whitespace**
- one hero subject
- hero subject centered or slightly lower-centered
- caption in left whitespace
- sparse doodles only

### Do not

- fill the whole page
- build a complex scene background
- create many equal focal points
- turn it into a crowded product collage
- use dense graphic layout

---

## 8. Photography-First Rule

The hero subject must remain photorealistic.

### Rules

- preserve realistic texture and material
- preserve object identity
- use soft studio-clean lighting
- keep the subject as photography, not illustration
- doodles must sit around the product, not replace it

If the main object becomes too cartoon-like, simplify and restore realism.

---

## 9. Quick Mode

Use Quick Mode when the user wants a fast complete result.

### Quick Mode must still include

- Subject Lock
- mandatory caption if provided
- locked micro-worker system
- product-related worker actions
- clean white-background layout
- photography-first rule

### Quick Mode definition

- one-pass complete poster
- best for first exploration
- acceptable if not perfect, but must still pass all hard rules

---

## 10. Fidelity Mode

Use Fidelity Mode when the user wants one aspect to become more accurate.

```yaml
mode: fidelity
fidelity_focus: subject_identity | dominant_element | lettering
```

### Hard rule

**Only one fidelity focus per pass.**

### `subject_identity`
Use when:
- the product changed category
- the object no longer looks like the original
- the key parts or material are wrong

Goal:
- restore object identity and realism

### `dominant_element`
Use when:
- the user says “强调最大的元素”
- the first visual focus is unclear
- the biggest meaningful feature needs stronger hierarchy

Goal:
- make the most meaningful large element become the first visual signal

### `lettering`
Use when:
- the title is missing
- the title is wrong
- the title looks too digital or too neat

Goal:
- freeze poster base and repair only the caption system

### Lettering Safety Rule

If a caption is important and the first pass misses or weakens it, the next repair should prefer **`fidelity_focus: lettering`**.

---

## 11. Final Prompt Assembly Requirement

Before generation, the final prompt must explicitly inline all critical rules.

The final prompt must include:

1. exact hero subject description
2. subject lock summary
3. caption text and mandatory placement if caption exists
4. locked micro-worker figure description
5. locked worker silhouette proportions: squat 2.2–2.8-head-tall body, oversized blank head, short stubby limbs
6. 3–5 product-related worker actions
7. no-default-ladder / grounded-prop rule
8. white-space composition rule
9. photography-first rule
10. selected mode and fidelity focus if applicable

### Important

Do **not** assume that “the model already knows” the caption or worker system.
Always restate them in the final generation prompt.

---

## 12. Post-Generation Self-Check

After generation, inspect the result against this checklist:

- Is the hero subject clear and correct?
- Is there only one main subject?
- Is the caption present if the user provided one?
- Is the caption rendered in thin, loose handwritten Chinese?
- Is the caption placed in left whitespace?
- Are the workers faceless and expressionless?
- Are the workers thin black line doodles only?
- Are the workers squat rather than long-limbed stick figures?
- Are worker bodies approximately 2.2–2.8 head diameters tall?
- Are all structural props grounded, and is there no unnecessary ladder?
- Are the worker actions product-related?
- Is the background still mostly white?
- Is the poster still calm and minimal?
- Is the product still photorealistic?

If any critical answer is **no**, the result must be treated as failed.

---

## 13. Repair Priority

If one repair pass is needed, repair in this order:

1. missing or incorrect caption
2. wrong subject identity
3. too many hero subjects / cluttered composition
4. wrong micro-worker silhouette / long-limbed stick-figure drift
5. unnecessary or floating structural props
6. weak visual hierarchy

Do not attempt unlimited retries. Use **one targeted repair pass**.

---

## 14. When to Use Two-Pass Generation

Default Quick Mode can be one-pass.

However, if any of the following is true, prefer a two-pass strategy:

- user gives a specific Chinese title
- user explicitly cares about handwriting style
- title is central to the joke or message
- the first pass tends to omit text

### Two-pass strategy

**Pass 1**
- build subject + workers + whitespace poster base
- keep composition stable

**Pass 2**
- repair / add caption and arrow
- preserve the poster base
- focus only on lettering quality and placement

This is strongly recommended for Codex execution stability.

---

## 15. Codex Execution Notes

This skill is designed to work in Codex-like environments where implicit conversational memory is weak.

Therefore:

- never rely on earlier chat preference memory
- never rely on “style intent” alone
- always inline hard constraints into the final generation prompt
- always perform self-check after generation
- always treat missing title and wrong worker style as hard failures

---

## 16. Minimal Prompt Skeleton

Use this as the minimum structure when assembling the final generation prompt:

```text
Generate a minimalist white-background poster.

Hero subject:
[exact real product description]

Caption:
Render the exact handwritten Chinese text: "[caption]".
This caption is mandatory.
Place it in the upper-left or left-side whitespace area.
Use thin black loose naive handwriting.
Add a simple hand-drawn arrow pointing toward the subject.

Micro-workers:
Add 3 to 5 tiny workers around the product.
They must have oversized blank round heads, no facial features, no expression, no hair, no clothing, a short compact rounded torso, short stubby arms and legs, white empty interiors, and thin uneven black single-line outlines only.
Each figure should be approximately 2.2–2.8 head diameters tall.
Do not generate long-limbed stick figures.
Each worker performs a different product-related action. Choose the action first, then add only the smallest necessary prop. Ladders, scaffolds, ropes, and floating structural props are forbidden by default.

Composition:
Pure white background.
Large whitespace.
One hero subject only.
Supporting props must stay secondary.
Hero subject centered or slightly lower-centered.

Style:
Photoreal product, soft studio lighting, calm, healing, restrained.
Do not cartoonize the product.
Do not omit the caption.
Do not turn the workers into mascots.
Do not use ladders or floating structural props unless explicitly required and physically grounded.
```

---

## 17. Success Definition

A successful result must simultaneously satisfy all of these:

- the subject is still the right subject
- there is one clear hero subject
- the title exists when provided
- the title looks handwritten, not typed
- the workers match the locked figure system
- the workers have squat 2.2–2.8-head proportions rather than stick-figure anatomy
- no unnecessary or floating ladder / structural prop appears
- the workers explain the product rather than decorate it randomly
- the poster keeps strong whitespace and a calm visual tone

If any of these fail, the result is not considered a correct execution of this skill.
