---
name: visual-creation
description: Style-governed image generation with quality gates. Manages visual style DNA, generates image prompts optimized for AI tools, and applies a council-review process before batch creation. Use when creating blog hero images, social graphics, thumbnails, product visuals, or any branded imagery.
---

# Visual Creation

Generate on-brand visuals using a defined style system, not vibes.

## How this skill works

Visual creation applies a 3-phase process:
1. **Load style DNA** — pull visual rules from `CREATOR.md` or `creator-memory/visual.md`
2. **Engineer prompt** — translate concept into a detailed image generation prompt
3. **Apply quality gates** — check against brand standards before approving

If no visual style is documented, prompt the user to describe their aesthetic or run `/creator-sprint`.

## Visual Style DNA

Before generating, confirm these parameters are known:

| Parameter | What to capture | Example |
|-----------|----------------|---------|
| Color palette | Primary + 2-4 accents | Deep navy, cyan, gold, white |
| Mood/aesthetic | Overall feeling | Dark premium, editorial, clean light |
| Subject preference | What appears in images | Technology, abstract concepts, humans |
| Composition | How elements are arranged | Rule of thirds, centered, dynamic |
| Style reference | Visual category | Glassmorphic, editorial photography, 3D render |
| Anti-patterns | What to avoid | Flat clip art, chrome robots, single-color saturation |

Load from `creator-memory/visual.md` if it exists. Otherwise ask.

## Prompt Engineering

A good image generation prompt has 6 components:

```
[Style/Medium] [Subject] [Setting/Context] [Mood] [Color Direction] [Technical Quality]
```

**Example (blog hero — dark premium tech)**:
```
Dark premium 3D render, glowing holographic interface floating above sleek desk surface,
dramatic cyan and gold lighting against deep navy background, depth of field blur on
background elements, cinematic composition, highly detailed, 8K quality, no text,
no humans, no chrome robot figures
```

**Example (social image — light editorial)**:
```
Clean editorial photograph, open laptop with code on screen, minimalist desk setup
with coffee cup and notebook, soft morning light from left, white and warm tones,
shallow depth of field, lifestyle photography style, high resolution
```

### Prompt modifiers by style type

| Style | Key modifiers |
|-------|--------------|
| Dark premium | dark background, dramatic lighting, deep shadows, cinematic, moody |
| Light editorial | white/light tones, natural light, minimal, clean, lifestyle photography |
| 3D render | 3D render, subsurface scattering, ray tracing, realistic materials |
| Illustration | digital illustration, vector-style, flat design, 2D |
| Glassmorphic | frosted glass, transparency, blur, depth layers, neon accents |
| Cinematic | film grain, letterbox, dramatic color grading, shallow depth of field |

## Quality Gates

Apply these checks before accepting an image. All gates must pass.

### 7-Gate Quality Filter

| Gate | Check | Fail condition |
|------|-------|---------------|
| 1. Brand alignment | Colors match palette | Wrong colors, off-brand feel |
| 2. Color balance | 3+ distinct tones | Single-color saturation, monochrome |
| 3. Composition depth | Foreground + midground + background | Flat, no depth |
| 4. Subject quality | Main subject is clear and intentional | Ambiguous, cluttered |
| 5. Text legibility | If text exists, it's readable | Blurry text, wrong font style |
| 6. Anti-pattern check | None of the defined anti-patterns | Contains vetoed elements |
| 7. Scroll-stop | Would this stop someone scrolling? | Generic, forgettable |

### Common anti-patterns (generic — customize in visual.md)

- Generic stock-photo feel (hands on keyboard, bland office)
- Single-color saturation (everything one hue)
- Chrome robots as primary subject (overused in AI imagery)
- Sparse composition (too much empty space, no depth)
- Flat clipart style (no depth or lighting)
- Inconsistent style mixing (editorial + 3D + illustration in one)

## Image Types by Use Case

| Type | Dimensions | Key requirements |
|------|-----------|-----------------|
| Blog hero | 1200×628 | No text, scroll-stop visual, brand colors |
| Social (LinkedIn) | 1200×627 | Works with text overlay, high contrast |
| Social (Twitter/X) | 1600×900 | Bold composition, clear focal point |
| Newsletter header | 1200×400 | Wider aspect ratio, simple |
| Thumbnail | 1280×720 | High contrast, readable at small size |
| Product hero | 1:1 or 4:5 | Clean, premium, minimal |
| Profile / avatar | 1:1 | Face visible, brand-aligned background |

## Output Format

When generating a visual prompt, deliver:
1. **Prompt** — ready to paste into the generation tool
2. **Negative prompt** — elements to exclude (if tool supports it)
3. **Rationale** — brief explanation of key choices
4. **Alternatives** — 1-2 prompt variations if the concept allows

After generation:
1. Apply quality gates
2. Report pass/fail on each gate
3. If fail: identify the specific gate and suggest prompt adjustment
4. If pass: add to image log if one exists (`creator-memory/image-log.md`)

## Tools

This skill is tool-agnostic — it engineers the prompt. Apply it with:
- `~~image generation` (any connected tool)
- Local tools: Gemini 2.5 Flash Image, Midjourney, Stability AI, Flux
- The prompt format works across all major image generation models

See `references/prompt-library.md` for tested prompts by category.
