# Poster Base Prompt

Prompt revision: **v0.7-worker-scale-calibration**

Use in Fidelity Mode for `subject_identity` or `dominant_element`.

This pass solves subject preservation, focus hierarchy, composition, photography, and worker storytelling only.

Do **not** generate any title or text in this pass.

```text
Create a minimalist white-space poster base from the uploaded reference photo.

PROMPT REVISION
v0.7-worker-scale-calibration

FIDELITY FOCUS
[fidelity_focus: subject_identity | dominant_element]

SUBJECT LOCK
Preserve the exact photographed subject: [exact category], [silhouette/proportions], [main color], [material], [defining toppings/details], and [plate/container/support relation]. Do not redesign, cartoonize, or reinterpret the object into another category.

SCENE LOCK
If the source is complex, preserve only 1–3 useful recognition cues: [scene cue 1], [scene cue 2], [optional cue 3]. Remove or simplify unrelated background clutter.

FOCUS LOCK
Primary focus element: [focus element].
Reason: [identity / size / shape / color / semantic importance].

If fidelity_focus = subject_identity:
- preserve category, silhouette, material, and defining details before creative exaggeration;
- keep only supporting cues necessary for recognition.

If fidelity_focus = dominant_element:
- make the selected focus the first photographic signal;
- normally scale it to about 45%–60% of canvas height depending on shape;
- keep only 0–2 photographic supporting cues;
- keep secondary photographic elements weaker in size, contrast, saturation, and placement;
- choose the largest meaningful subject element rather than literal background architecture.

PHOTOGRAPHY
Keep the hero fully photographic with realistic material, surface texture, highlights, translucency/gloss/moisture/cream/fruit/glass behavior as relevant. Use clean high-key studio soft light, low contrast, and a soft natural contact shadow.

COMPOSITION
Pure white or lightly warm-white field.
For subject_identity, target about 70%–80% negative space when possible.
For dominant_element, allow about 60%–70% if stronger scale is needed.
Reserve clean empty title space in the upper-left or left side.

MICRO WORKERS — CALIBRATED FIGURE LOCK
Add 3–5 very small primitive black-line workers.

Identity:
- blank round or slightly irregular head
- no eyes, mouth, nose, eyebrows, or expression
- no hair, hats, clothing details, labels, logos, badges, or body symbols
- white empty interior
- thin uneven black single-line outline

Proportions:
- total figure height about 2.8–3.5 head diameters
- head about 28%–35% of total figure height
- torso width about 55%–75% of head diameter
- torso short and lightly rounded, not broad/barrel-shaped
- arms and legs slim and short-to-medium
- almost no visible neck

Do not generate:
- giant-headed chibi figures
- fat/squat barrel bodies
- thick stubby limbs
- long-limbed stick figures
- thin adult doodle humans
- realistic anatomy
- polished mascots

RELATIVE SCALE LOCK
Workers must remain miniature relative to the hero:
- normal worker height = about 12%–18% of hero subject height
- preferred average = about 14%–16%
- no worker above 20% of hero height unless explicitly requested
- product must visually dominate before any worker is noticed

ACTION SELECTION
Choose action first, then the smallest useful prop.
Prefer: hold, carry, push, pull, wipe, scoop, arrange, collect, inspect, taste, clean, cool, fan, rest, shade.
Use selectively: pour, water, measure, repair.

STRUCTURAL PROP BUDGET
Default = 0 structural props.
Maximum = 1 per poster.
A ladder/stool/step is allowed only when vertical access genuinely improves the product story.
Never add one only because the product is tall.
If used:
- base visibly rests on the ground plane
- perspective matches the product
- top visibly contacts a stable surface/product edge when appropriate
- worker hands/feet physically connect
- no floating or ending in empty space

Ropes, scaffolds, suspended lines, and floating platforms remain disallowed unless explicitly requested.

Actions:
1. [feature → direct worker action]
2. [feature → direct worker action]
3. [feature → direct worker action]
4. [feature → direct worker action]
5. [optional]

Every action must physically or causally relate to a real product feature. In dominant_element mode, workers should interact with the Focus Lock element first.

TEXT CONSTRAINT
No title, no Chinese characters, no English letters, no numbers, no captions, no labels, no pseudo-text, no watermark, no logo. Leave title area clean for a later lettering layer.

COLOR
Use only subject-derived colors + white + black doodles.

FINAL SELF-CHECK
- workers are small relative to hero, normally 12%–18%, max 20%
- workers are 2.8–3.5 heads tall with narrow lightly rounded torso
- no fat/chibi workers
- no long-limbed stick figures
- structural prop count is 0 by default and max 1
- any ladder/stool is physically grounded
- no rope, scaffold, suspended line, or floating platform
- every worker action relates to a real product feature

If worker scale or silhouette fails, repair the poster base before continuing to lettering.

OVERALL
Quiet, premium, healing, minimal, lightly humorous. Real product photography remains the hero; the doodle workers stay visually small and secondary.
```
