# Visual Soul Product Photography

A reusable Codex skill for turning authorized product images and a visual reference board into original lifestyle-product photography.

It is designed for the point between a generic prompt and a rigid campaign copy: images should feel observed, tactile, and alive while the product remains physically recognizable.

## What It Reuses

- Separates **product fidelity** from **visual inspiration**.
- Extracts a compact visual-soul card instead of copying a reference image.
- Uses 35mm, 50-58mm, and 85mm as distinct storytelling roles.
- Builds a candidate pool before choosing final images.
- Reviews candidates for life, product integrity, physics, light, and lens coherence.
- Revises the single failing layer instead of piling on negative prompts.

## Install

Clone or download this repository, then copy the skill directory into your Codex skills folder:

```bash
cp -R visual-soul-product-photography ~/.codex/skills/
```

Restart Codex or start a new task so it discovers the skill.

## Use

Provide:

1. One or more product images. Include different angles for objects with important construction details.
2. A 4-12 image style board. Use images you are authorized to share.
3. A visual soul card based on `references/soul-card-template.md` when the work will be repeated across a brand or collection.
4. A short outcome request: product use, place or audience, and desired number of final images.

Example:

```text
Use $visual-soul-product-photography.
Image 1-3 are my product from different angles. Images 4-9 are the visual soul board.
Create a 9-image candidate pool for a compact water bottle used in bright, unforced city life.
Start with three 35mm environmental frames, three 50-58mm everyday-use frames,
and three 85mm observational details. Select the strongest candidate from each lens role.
```

## Recommended Workflow

1. Generate 3-4 candidates for each intended lens role.
2. Score them with `references/review-card.md`.
3. Keep the strongest one per role.
4. Revise only the weakest layer, such as light, action, product geometry, or camera behavior.
5. Use a compositing pass for exact small labels or logos when required.

## API Providers

The skill works with any image provider chosen by the user. `references/openai-compatible-images-api.md` explains how to connect an OpenAI-compatible Images API without hardcoding a vendor, endpoint, or credential in this repository.

## Before Publishing

- Remove personal product images, client work, internal style boards, request responses, and credentials.
- Confirm you have permission to redistribute every example image.
- Choose a license that matches how you want other people to use the workflow.

## License

MIT. See [LICENSE](LICENSE). The skill's text workflow is open to reuse; it does not grant rights to any product photos, style references, logos, or campaign imagery that a user supplies.

## Repository Layout

```text
visual-soul-product-photography-skill/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── openai-compatible-images-api.md
    └── review-card.md
    └── soul-card-template.md
```
