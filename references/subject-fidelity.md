# Subject Fidelity Guide

## First rule: identify before stylizing

Before inventing captions, metaphors, workers, or props, answer:

> What exactly is the photographed object?

Lock the answer before continuing.

## Subject Lock fields

When a reference image is provided, internally resolve:

```yaml
category: exact product / food type
silhouette: primary outer shape and proportions
main_color: dominant real color
material: gloss, jelly, glass, fruit flesh, fabric, metal, etc.
toppings_or_details: visible defining elements
support_relation: plate, cup, bottle, tray, container, stand when important
must_preserve: details that make the object recognizable
can_remove: unrelated environmental clutter
```

## Priority order

```text
subject identity
> source shape/material/color
> style transformation
> micro-story creativity
```

A stronger metaphor is never a reason to change the product category.

## Known regression example

Source:

```text
blue molded pudding + whipped cream + red cherry + white plate
```

Incorrect transformation:

```text
blue shaved ice mountain
```

Why it failed:

- the model over-weighted “blue / cold / refreshing”;
- the physical category was not locked early enough;
- the story metaphor replaced the object rather than interacting with it.

Correct behavior:

```text
keep the molded blue pudding recognizable;
keep its smooth glossy pudding surface;
keep whipped cream and cherry;
keep the white plate when it helps recognition;
let workers act on the pudding without turning it into another dessert.
```

## Busy-source cleanup

The skill may simplify the source environment while preserving the hero object.

Normally remove:

- unrelated tableware;
- books;
- background desserts;
- room details;
- visible watermarks from the composition when legally and technically appropriate;
- clutter that competes with the hero.

Normally preserve:

- the chosen product;
- its important garnish;
- a plate/container if it defines the product presentation;
- material-specific highlights and shadows.

## Multi-subject rule

If the user clearly identifies the subject, use it.

If not, and the photo contains several independent plausible subjects, ask the user to choose rather than silently selecting the most food-like or colorful object.

A container and its contents count as one subject by default.

## Fidelity checklist

Before generation, verify:

- [ ] exact category is known;
- [ ] silhouette is described;
- [ ] material is described;
- [ ] main color is preserved;
- [ ] defining garnish/detail is preserved;
- [ ] environmental clutter is separated from the hero;
- [ ] no creative metaphor changes the object type.

## Repair instruction

If the object drifts:

```text
Regenerate the poster while locking the source object first. Preserve the exact product category, silhouette, proportions, material, main colors, garnish, and plate/container relationship. Do not reinterpret the subject into another food or object. Change only the background simplification, doodle interaction, and composition.
```