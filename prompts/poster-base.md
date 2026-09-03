# Poster Base Prompt

Prompt revision: **v0.6-worker-shape-lock**

Use in Fidelity Mode for `subject_identity` or `dominant_element`.

This pass solves subject preservation, focus hierarchy, composition, photography, and worker storytelling only.

Do **not** generate any title or text in this pass.

```text
Create a minimalist white-space poster base from the uploaded reference photo.

PROMPT REVISION
v0.6-worker-shape-lock

FIDELITY FOCUS
[fidelity_focus: subject_identity | dominant_element]

SUBJECT LOCK
Preserve the exact photographed subject: [exact category], [silhouette/proportions], [main color], [material], [defining toppings/details], and [plate/container/support relation]. Do not redesign, cartoonize, or reinterpret the object into another category.

SCENE LOCK
If this is a complex scene, preserve only these 1–3 recognition cues: [scene cue 1], [scene cue 2], [optional scene cue 3]. Remove or simplify all unrelated source-background clutter.

FOCUS LOCK
Primary focus element: [focus element].
Reason: [identity / size / shape / color / semantic importance].

If fidelity_focus = subject_identity:
- preserve the source object's category, silhouette, material, and defining details before any creative exaggeration;
- do not distort one element so much that it becomes a different product;
- keep only supporting cues necessary for recognition.

If fidelity_focus = dominant_element:
- make the selected focus element the first photographic signal;
- normally scale it to about 45%–60% of canvas height depending on shape;
- keep only 0–2 photographic supporting cues;
- keep all secondary photographic elements weaker in size, contrast, saturation, and placement;
- if the literal largest area is irrelevant background architecture, emphasize the largest meaningful subject element instead.

PHOTOGRAPHY
Keep the hero object fully photographic with realistic material, surface texture, highlights, translucency/gloss/moisture/cream/fruit/glass details as relevant. Use clean high-key studio soft light, low contrast, and a soft natural contact shadow.

COMPOSITION
Pure white or very lightly warm-white field.

For subject_identity, keep approximately 70%–80% negative space when possible.
For dominant_element, keep generous negative space but allow approximately 60%–70% when the focus element needs stronger scale.

Place the hero center-lower or another intentionally quiet lower position. Reserve a clean empty title area in the upper-left or left side. Do not let secondary photographic elements compete with the Focus Lock.

MICRO WORKERS — HARD SILHOUETTE LOCK
Add [3–5] tiny primitive black-line workers around the product.

Every worker must use the same fixed body geometry:
- oversized blank round or slightly lumpy head
- head occupies about 35%–45% of total figure height
- total figure height about 2.2–2.8 head diameters
- almost no visible neck
- short compact rounded torso
- short stubby arms
- short stubby legs
- tiny rounded hand and foot ends
- white empty interior
- thin uneven black single-line outline only
- no eyes, mouth, nose, eyebrows, or expression
- no hair
- no hats
- no clothing details
- no labels, logos, badges, or body symbols

The silhouette must feel squat, soft, primitive, and slightly clumsy.

FORBIDDEN FIGURE SHAPES
Do not generate:
- stick figures
- long thin arms
- long thin legs
- thin adult doodle humans
- realistic human anatomy
- 4–6 head-tall bodies
- fashion-illustration proportions
- polished mascot silhouettes

ACTION SELECTION
Choose the action first. Then add only the smallest possible prop if the action cannot be understood without it.

Prefer direct-contact actions:
hold, carry, push, pull, wipe, scoop, arrange, collect, inspect, taste, clean, cool, fan, rest, shade.

Use selectively:
pour, water, measure, repair.

FORBIDDEN BY DEFAULT
Do not use:
- climb
- ladder
- stairs
- scaffold
- rope
- suspended line
- platform
- floating structural prop

These are forbidden unless the user explicitly requests them.

PROP GROUNDING
Every physical prop must obey believable spatial physics:
- visible support
- same ground plane as the product
- correct perspective
- no floating
- no ending in empty space
- no leaning without visible contact
- worker hands or feet must visibly connect to the prop

If spatial grounding is unclear, remove the prop completely.

Actions:
1. [feature → direct worker action]
2. [feature → direct worker action]
3. [feature → direct worker action]
4. [feature → direct worker action]
5. [optional]

Every action must physically or causally relate to a real product feature. In dominant_element mode, workers should interact with the Focus Lock element first.

TEXT CONSTRAINT
No title, no Chinese characters, no English letters, no numbers, no captions, no labels, no pseudo-text, no watermark, no logo. Leave the title area completely clean for a later lettering layer.

COLOR
Use only subject-derived colors + white + black doodles.

FINAL SELF-CHECK
Before accepting this poster base, verify:
- workers are squat 2.2–2.8-head-tall figures
- heads are oversized relative to bodies
- arms and legs are short and stubby
- no long-limbed stick figures appear
- no ladder, rope, scaffold, stairs, suspended line, or floating platform appears
- every prop is visibly grounded
- every worker action relates to a real product feature

If any worker is long-limbed or any forbidden structural prop appears, treat the poster base as failed and repair it before continuing to lettering.

OVERALL
Quiet, premium, healing, minimal, lightly humorous. Real product photography remains the visual hero; doodles remain secondary. The selected Fidelity Focus must be obvious even at thumbnail size.
```