---
name: music-production
description: AI music generation pipeline for creators using Suno AI and compatible tools. Engineers detailed prompts, manages style consistency across tracks, and documents production decisions. Use when creating music for content, brand identity, products, or creative projects.
---

# Music Production

Engineer precise prompts for AI music generation — consistent style, not random output.

## How this skill works

Music production for creators follows a 4-step pipeline:
1. **Define** — clarify purpose, mood, and audience
2. **Style load** — pull music style from `creator-memory/music.md`
3. **Prompt engineer** — build the Suno (or compatible) prompt
4. **Document** — log the output for style consistency

## Music Purpose Framework

Before engineering a prompt, establish intent:

**Purpose questions:**
- What transformation should the music facilitate? (energy, focus, relaxation, inspiration)
- Who is the listener and what state are they in when they hear this?
- What state should they be in after?
- What's the use case? (background music, intro jingle, content underscore, standalone track)

**Use case categories:**
- **Background** — ambient, non-distracting, supports work or focus
- **Content underscore** — supports video/podcast, mixes under narration
- **Intro/outro** — brand signature, 10-30 seconds, memorable
- **Standalone track** — complete song, can be listened to independently
- **Atmospheric** — scene-setting, emotional, immersive

## Suno Prompt Formula

```
[Genre/Style], [Tempo descriptor], [Key instruments], [Vocal style or "no vocals"], [Mood descriptors], [Special elements]
```

**Component breakdown:**

| Component | Examples |
|-----------|---------|
| Genre/Style | lo-fi hip hop, cinematic orchestral, dark ambient, future bass, neo-soul |
| Tempo | slow, mid-tempo, uptempo, driving, laid-back, pulsing |
| Key instruments | piano, synth pads, acoustic guitar,808s, strings, brass, choir |
| Vocal style | no vocals, ethereal female vocals, deep male narrator, spoken word, chopped vocals |
| Mood | melancholic, triumphant, mysterious, uplifting, tense, meditative, euphoric |
| Special elements | layered textures, build and drop, minimal and spacious, lush reverb, distorted |

**Example prompts:**

*Focus/productivity music:*
```
Lo-fi hip hop, slow mid-tempo, warm piano melodies over dusty drums, mellow bass,
no vocals, nostalgic and focused mood, vinyl crackle, smooth and unobtrusive
```

*Epic cinematic intro:*
```
Cinematic orchestral, building tempo, full strings and brass, choir build in final section,
no main vocals, triumphant and expansive mood, dramatic crescendo, Hollywood film score style
```

*Meditation/ambient:*
```
Dark ambient, very slow, deep synth drones, distant piano notes, no vocals,
introspective and vast mood, heavy reverb, sound design elements, mysterious and meditative
```

*Brand intro jingle (10-20 sec):*
```
Electronic pop, upbeat, bright synth lead, punchy kick, no vocals,
optimistic and forward-moving mood, modern and clean production,
memorable 4-bar hook, designed for intro/logo placement
```

## Style Consistency

To maintain consistent sound across multiple tracks:
1. Document successful prompts in `creator-memory/music.md`
2. Note which elements create the desired sound
3. Use the same core descriptors across related tracks, varying only the mood/energy
4. Mark "anchor tracks" — reference tracks that define the style

**Style anchor format:**
```markdown
## Style Anchor: [Track Name]
- Core genre: [genre]
- Essential elements: [list]
- Avoid: [list]
- Use for: [context]
- Suno prompt: [full prompt]
```

## Music Style Categories for Creators

| Category | Best for | Typical elements |
|----------|---------|-----------------|
| Lo-fi study beats | Productivity content, background | Warm piano, dusty drums, vinyl crackle |
| Cinematic orchestral | High-production video intros, emotional content | Strings, brass, choir, building |
| Dark ambient | Introspective content, meditation | Drones, reverb, minimal, mysterious |
| Future bass | Energetic content, tutorials, hype | Synth leads, wobble bass, punchy drums |
| Neo-soul | Lifestyle content, warm brand feel | Soulful vocals, jazz chords, groove |
| Minimal electronic | Clean product videos, corporate | Sparse, precise, modern, functional |
| Acoustic indie | Personal content, authenticity | Guitar, soft percussion, intimate |

## Track Documentation

Log every generated track for style consistency:

```markdown
## Track: [Title]
- Date: [YYYY-MM-DD]
- Use case: [context]
- Suno prompt: [full prompt]
- Score (1-10): [rating]
- Keep: [yes/no]
- Notes: [what worked, what didn't]
```

Save to `creator-memory/music.md`.

## Quality Check

Before using a generated track:
1. **Purpose fit** — does it serve the intended use case?
2. **Consistency** — does it match the established brand sound?
3. **Quality** — no obvious artifacts, loops are clean, fades are smooth
4. **Rights** — confirm generation platform's commercial use terms

## Output Format

When engineering a prompt, deliver:
1. **Prompt** — ready to paste into Suno or compatible tool
2. **Purpose alignment** — confirm it fits the stated use case
3. **Style notes** — what elements drive the desired sound
4. **Variations** — 2 alternative prompts for different energy levels
