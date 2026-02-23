---
description: Engineer a Suno AI prompt and document the track for your music production pipeline
argument-hint: "<style or mood or use case>"
---

# Create Music

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a precise music prompt for Suno AI or compatible music generation tools, aligned with your established sound and use case.

## Workflow

### 1. Understand the Request

Accept any of:
- A use case ("intro music for my YouTube channel")
- A mood ("something for deep work focus")
- A style ("lo-fi but with jazz chords")
- A context ("background music for a cinematic product demo video")
- A project tie-in ("music for the Arcanea project — mysterious, mythological")

If unclear, ask: "What's this music for, and what feeling should it create?"

### 2. Load Music Style

Check `CREATOR.md` or `creator-memory/music.md` for:
- Established music style (genre anchors)
- Style anchor tracks (reference prompts that define the sound)
- Use cases already defined (focus, intros, content, etc.)

If no music style is documented, proceed with user description and offer to save the result as a style anchor.

### 3. Establish Parameters

Confirm before writing the prompt:
- **Use case**: background / intro-outro / standalone / content underscore
- **Mood**: (see `music-production` skill for category list)
- **Length**: short (30-60s) / standard (2-3 min) / long (3-5 min)
- **Vocals**: yes (specify style) / no

### 4. Engineer the Prompt

Apply the Suno formula from the `music-production` skill:
```
[Genre/Style], [Tempo], [Key instruments], [Vocal style], [Mood descriptors], [Special elements]
```

Build for:
- Purpose fit — the prompt should create music that works for the stated use
- Style consistency — use the same core descriptors as existing anchors if they exist
- Specificity — vague prompts produce generic music

### 5. Deliver

Present:
1. **Primary prompt** — ready to paste into Suno or compatible tool
2. **Prompt rationale** — why these elements create the desired sound
3. **Variation prompts** — 2 alternatives (one higher energy, one lower)
4. **Documentation template** — ready to fill in after generation

### 6. Post-Generation (if result is described)

If the user describes or rates the generated track:
- Log it to `creator-memory/music.md` if it's worth keeping
- Extract what worked for use in future prompts
- Update style anchor if this track sets a new standard

## Output Format

```
**Prompt:**
[Full Suno prompt]

**Rationale:**
[Why these elements create the desired sound]

**Variations:**
1. [Higher energy version]
2. [More ambient/subdued version]

**Track log (fill in after generation):**
- Title: [working title]
- Date: [today]
- Use case: [context]
- Score: [1-10 after listening]
- Keep: [yes/no]
- Notes: [what worked]
```

## Tips

- Suno responds well to layered descriptors: genre + tempo + instruments + mood in that order
- "No vocals" is its own descriptor — always include if you don't want singing
- For brand music, prioritize consistency over variety — similar prompts across tracks create a coherent sound
- Short intro tracks (10-20s) need "designed for intro/logo placement" or similar cue
- If a track is close but not right, refine one element at a time rather than rewriting the whole prompt
