# Fidelity Focus System

Fidelity Mode should not mean “make everything more detailed.” It should solve one fidelity problem at a time while protecting the accepted parts of the poster.

Use one explicit focus:

```yaml
mode: fidelity
fidelity_focus: subject_identity | dominant_element | lettering
```

If the user does not name the focus, infer it from intent:

- “还原主体 / 不要改产品 / 保持原物” → `subject_identity`
- “强调最大的元素 / 突出番茄 / 把饼干做大” → `dominant_element`
- “字体不像 / 只改标题 / 不要动其他地方” → `lettering`

## Shared lock hierarchy

Fidelity Mode uses three locks. They solve different problems and must not overwrite one another.

### 1. Subject Lock

Answer: **What is the photographed object?**

Lock category, silhouette, material, color, defining topping/details, and important container/support relation.

### 2. Scene Lock

Answer: **What makes this source scene recognizable?**

Use only when the source is a complex installation, table scene, display, or multi-object composition. Keep 1–3 scene cues that matter to recognition; remove the rest.

Example:

```text
vegetable farm installation
scene cues = giant red tomato + pink plush vegetable figure + broccoli group
```

Scene Lock is not permission to copy every source object into the poster.

### 3. Focus Lock

Answer: **What must become the first visual signal in this Fidelity pass?**

The selected `fidelity_focus` controls this lock.

---

## Focus A — subject_identity

Use when the source object itself must stay faithful.

Priority:

```text
category > silhouette > material > defining details > composition invention
```

Rules:

- Do not reinterpret the product category.
- Do not exaggerate one detail so much that the object becomes a different product.
- Preserve the strongest source cues before designing workers.
- Simplify the background rather than redesigning the hero.
- Keep supporting photographic elements only when they are necessary for recognition.

Success question:

> If the source and result are shown side by side without text, is it obviously the same object?

---

## Focus B — dominant_element

Use when the user asks to emphasize the largest, strongest, or most distinctive visual element.

Before generation, explicitly identify:

```yaml
focus_element: [largest / strongest element]
focus_reason: [size / shape / color / semantic importance]
```

Rules:

- The focus element becomes the first photographic signal.
- It should normally occupy about 45%–60% of canvas height depending on shape.
- Keep generous white space; around 60%–70% may be acceptable when a large focus element needs more presence.
- Reduce secondary photographic subjects to 0–2 supporting cues.
- Secondary elements must not compete in size, saturation, contrast, or placement.
- Workers should physically interact with the focus element first.
- Caption meaning should connect to the focus element when possible.
- Do not invent a new giant object that did not exist in the source.
- If the largest visible thing is only background architecture or irrelevant clutter, choose the largest **meaningful subject element**, not the literal largest pixel area.

Examples:

```text
vegetable farm → giant red tomato
seafood soup → central yellow character-shaped ingredient
caramel ice cream → large caramel biscuit
apple tea → red apple / apple slices when the caption depends on “苹”
```

Success question:

> At thumbnail size, can a viewer identify the intended focus element before noticing the workers or secondary props?

---

## Focus C — lettering

Use when the accepted poster is already good and only the Chinese title needs repair.

Rules:

- Freeze the poster base completely.
- Do not regenerate the product, workers, lighting, or composition.
- Read `references/lettering-guide.md`.
- Generate only the lettering layer.
- Repair glyph skeleton, spacing, tilt, scale, stroke length, and baseline irregularity.
- Composite the accepted title onto the unchanged poster base.

Success question:

> Did the lettering improve without changing any accepted visual element underneath it?

---

## Single-focus rule

One Fidelity pass should have one primary focus.

Bad:

```text
make the product more faithful + make the tomato much bigger + completely redesign the title + add more workers
```

Good:

```text
Pass 1: dominant_element → emphasize giant tomato
Pass 2 if needed: lettering → repair title only
```

When several problems exist, solve them sequentially. This prevents one correction from washing away another accepted result.

## Output note

When writing a Fidelity prompt, state the focus in plain language near the top:

```text
FIDELITY FOCUS: DOMINANT ELEMENT
The giant red tomato is the first visual priority. Preserve its realistic photographic surface and make all other photographic elements clearly secondary.
```
