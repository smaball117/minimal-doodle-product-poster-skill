# Poster Base Prompt

Use in Fidelity Mode for `subject_identity` or `dominant_element`.

This pass solves subject preservation, focus hierarchy, composition, photography, and worker storytelling only.

Do **not** generate any title or text in this pass.

```text
Create a minimalist white-space poster base from the uploaded reference photo.

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

MICRO WORKERS
Add [3–5] tiny black-line workers around the product. Fixed figure contract: blank round or slightly lumpy head, no eyes, mouth, nose, eyebrows, or expression, no hair, no hats, no clothing details, no labels, no logos, no badges, no body symbols. Use simple uneven hand-drawn single-line bodies.

Actions:
1. [feature → action]
2. [feature → action]
3. [feature → action]
4. [feature → action]
5. [optional]

Every action must physically or causally relate to a real product feature. In dominant_element mode, workers should interact with the Focus Lock element first. Use only minimal action-serving props.

TEXT CONSTRAINT
No title, no Chinese characters, no English letters, no numbers, no captions, no labels, no pseudo-text, no watermark, no logo. Leave the title area completely clean for a later lettering layer.

COLOR
Use only subject-derived colors + white + black doodles.

OVERALL
Quiet, premium, healing, minimal, lightly humorous. Real product photography remains the visual hero; doodles remain secondary. The selected Fidelity Focus must be obvious even at thumbnail size.
```