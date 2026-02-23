---
description: Generate a brand-aligned image prompt with quality gates, ready for any AI image generation tool
argument-hint: "<concept or brief>"
---

# Create Visual

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a high-quality image prompt aligned with the creator's visual style, apply quality gates, and deliver the prompt ready for any image generation tool.

## Workflow

### 1. Understand the Request

Accept any of:
- A concept ("hero image for my blog post about AI agents")
- A use case ("LinkedIn header for my AI Architect positioning")
- A specific type ("thumbnail for a video about 10,000 AI songs")
- A vague aesthetic ("something dark and premium for my newsletter")

If the brief is very vague, ask one question to sharpen the visual concept.

### 2. Load Visual Style

Check `CREATOR.md` or `creator-memory/visual.md` for:
- Aesthetic direction (dark premium, light editorial, etc.)
- Primary and accent colors
- Composition preferences
- Anti-patterns to avoid
- Reference tracks (existing images that define the style)

If no visual style is documented, ask: "What's your visual aesthetic? (e.g., dark and dramatic, clean and minimal, colorful and bold)"

### 3. Determine Image Parameters

Establish before writing the prompt:
- **Type**: blog hero / social post / newsletter header / thumbnail / product visual / profile
- **Dimensions**: match to use case (see `visual-creation` skill for sizes)
- **Subject**: what's in the image? (technology, abstract, scene, lifestyle)
- **Text in image?**: usually no — confirm

### 4. Engineer the Prompt

Apply the 6-component formula from the `visual-creation` skill:
```
[Style/Medium] [Subject] [Setting/Context] [Mood] [Color Direction] [Technical Quality]
```

Include negative prompt elements (what to exclude) based on anti-patterns.

### 5. Apply Quality Gates

Before delivering, check the prompt against the 7 quality gates:
- [ ] Brand colors referenced in prompt
- [ ] 3+ distinct tones/colors specified
- [ ] Depth cues (foreground/background) included
- [ ] Clear focal subject
- [ ] No banned elements in prompt
- [ ] Composition direction specified
- [ ] Would generate a scroll-stopping result?

If any gate fails, refine the prompt before delivering.

### 6. Deliver

Present:
1. **Primary prompt** — optimized, ready to paste
2. **Negative prompt** — elements to exclude (if tool supports)
3. **Rationale** — 2-3 sentences on the key choices
4. **Variation prompts** — 2 alternatives (different mood or composition)
5. **Recommended tool settings** — size, steps, guidance scale if relevant

After delivery, offer:
- "Once generated, paste the result back and I'll score it against the quality gates."
- "Want a prompt for the same concept in [different style]?"

### 7. Post-Generation Review (if image is shared)

If the user shares the generated image, apply quality gates:
1. Check each of the 7 gates
2. Report pass/fail
3. If any fail: provide specific prompt adjustment

If pass: offer to log to `creator-memory/image-log.md`.

## Output Format

```
**Prompt:**
[Full image generation prompt]

**Negative prompt:**
[Elements to exclude]

**Rationale:**
[Brief explanation of key choices]

**Variations:**
1. [Alternative prompt 1 — different energy]
2. [Alternative prompt 2 — different composition]
```

## Tips

- Be specific with colors: "deep navy #0A0F1C with cyan accents" beats "dark blue"
- Include depth: foreground, midground, background elements — flat images fail the gate
- Name the anti-patterns explicitly in the negative prompt
- Generate one test image before committing to a style for a whole project
