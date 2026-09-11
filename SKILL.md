---
name: visual-soul-product-photography
description: Create candid product lifestyle photography from an authorized product image and a user-supplied visual soul board. Use when a physical product needs credible, non-staged lifestyle scenes rather than catalog packshots.
---

# Visual Soul Product Photography

Turn an authorized product image and a small visual reference board into an original lifestyle-photo candidate set. The objective is not to copy a reference. It is to translate its visual relationships into new scenes while keeping the product recognizable and physically credible.

## Inputs

Ask for only what is needed:

1. **Product reference**: at least one clear image of the product. Multiple angles are strongly preferred for objects with closures, controls, hardware, or printed markings.
2. **Visual soul board**: 4-12 references that the user is authorized to share. Label whether each one informs mood, light, action, composition, or material texture.
3. **Brief**: intended product use, place or audience if known, and whether the user wants a single shot or a candidate pool.

Do not treat a product packshot as a scene reference. Do not treat style references as products to copy.

## Extract the visual soul

Before prompting, create a concise internal soul card from the reference board. For a reusable brand system, save it using [the soul-card template](references/soul-card-template.md):

- **Human rhythm**: walking, pausing, conversation, carrying, making, resting, or another ordinary action.
- **Light**: available daylight, direction, softness, contrast, exposure tolerance, and reflection behavior.
- **Place and material**: plausible setting, surfaces, local objects, background density, and weather.
- **Camera behavior**: lens role, height, distance, crop, focus, foreground obstruction, motion, and imperfections.
- **Color and texture**: palette, grain, fabric, skin, pavement, wood, metal, paper, or other tactile signals.
- **Taste floor**: what makes the board feel alive rather than staged.
- **Avoid list**: only the specific failure modes visible from the brief, such as hard-ad posing, glossy CGI, contradictory light, or e-commerce composition.

Describe relationships, not brand names, creators, campaigns, or a reference's exact layout.

## Product preservation

List the product invariants before generating: silhouette, proportions, material finish, seams, controls, closures, handles or straps, hardware, openings, scale, and required markings. State that the supplied product is an authorized reference and its geometry must remain recognizable.

For small exact words, logos, labels, or screens, generation may drift. Treat a correct mark as a post-production or compositing requirement unless the user accepts approximate text.

## Shot design

Let life lead and allow the product to participate naturally. Choose one simple action that can happen without choreography. Hands, weight, straps, hinges, openings, and contact must follow normal physical logic.

Use lens roles as a series scaffold:

- **35mm**: environmental context, ordinary place, movement through the frame, breathing room, foreground interruption.
- **50-58mm**: an intimate real-use action, enough context to feel unarranged.
- **85mm**: observational detail, natural compression, a product feature visible through an active moment.

Do not force every shot to show the same gesture. Vary the situation before varying the product angle.

## Candidate-pool workflow

For a final three-image series, start with 9-12 candidates: 3-4 candidates per lens role. Each prompt must have a distinct everyday situation, not merely a different background.

Review candidates with [the scoring card](references/review-card.md). Keep the strongest frame per lens, then revise only its failing layer: product preservation, action, light, camera behavior, or styling. Do not add broad restrictions after one bad output.

## Prompt contract

Write generator-ready prompts in this order:

```text
REFERENCE MODE — authorized product preservation plus high-level style-board inspiration
PRODUCT — identity-critical features that must remain unchanged
SOUL — translated visual variables from the board
SCENE — plausible place, time, surfaces, background activity
ACTION — one simple, physically executable moment
LENS / CAMERA — focal length, distance, viewpoint, crop, focus behavior
LIGHT — source direction, softness, shadow and reflection logic
COMPOSITION — spatial layers, scale, foreground relationship, allowed imperfection
TASTE FLOOR — candid, alive, premium editorial photography; never a hard ad
TARGETED NEGATIVE — only likely failure modes for this shot
```

## Quality floor

- Product geometry, contact, scale, and weight must make sense.
- Human anatomy, grips, shadows, reflections, and perspective must agree.
- Keep a dominant plausible light source.
- Permit partial crops, background occlusion, mild motion softness, and slight exposure variation when they make the scene feel observed.
- Avoid white-background packshots, product grids, direct eye-contact posing, stiff fashion posture, generic hero landscapes, copy-like campaign frames, plastic CGI, and impossible anatomy unless the user explicitly asks for them.

## Provider choice

Use the image provider explicitly selected by the user or the current environment. For an OpenAI-compatible Images API, read [the provider guide](references/openai-compatible-images-api.md). Do not embed API keys, endpoints, or private reference images in this skill or in a public repository.
