---
name: creator-memory
description: Two-tier brand memory system for creators. Stores voice DNA, visual style, music style, channel rules, and active projects so Claude works as a true creative collaborator. CREATOR.md for working memory, creator-memory/ directory for the full knowledge base.
---

# Creator Memory

Memory makes Claude your creative collaborator — someone who knows your voice, your style, and what you're working on.

## The Goal

Transform shorthand into full creative context:

```
User: "write a linkedin post about the suno drop"
              ↓ Claude decodes
"Write a LinkedIn post in Frank's 'cool authority' voice about the
 release of 12,000+ Suno-generated tracks to the public library —
 connect to the AI Creator audience, don't lead with numbers, use
 fragment rhythm, no exclamation marks"
```

Without memory, that request requires extensive explanation. With memory, Claude knows:
- **suno drop** → the release of 12,000+ AI tracks to the public library
- **Frank's voice** → cool authority, fragment rhythm, no CTAs like "drop a comment"
- **linkedin post** → professional tone, thought-provoking opener, under 1,300 chars

## Architecture

```
CREATOR.md                    ← Working memory (voice, style, active projects)
creator-memory/
  voice.md                    ← Full voice documentation
  visual.md                   ← Visual style DNA
  music.md                    ← Music style and track log
  channels.md                 ← Per-channel rules
  projects/                   ← Active and archived project briefs
    {project-name}.md
  content/                    ← Content catalog (optional)
    published.md
    drafts.md
```

**CREATOR.md (Working Memory):**
- Active voice attributes and DO/DON'T examples
- Current content pillars (3-5)
- Active projects (name + 1-line brief)
- Channel-specific notes
- Frequently referenced terminology (products, concepts, names)
- **Goal: Cover 90% of daily creative requests**

**creator-memory/ (Deep Memory):**
- Full voice documentation with examples
- Complete visual and music style systems
- Per-channel deep rules
- Project archives with full briefs

## Lookup Flow

```
User request →
1. Check CREATOR.md (hot cache)
   → Voice attributes? ✓
   → Current project? ✓
   → Terminology? ✓

2. If not found → search creator-memory/
   → voice.md for full voice rules
   → visual.md for style rules
   → projects/ for project context

3. If still not found → ask user
   → "What should I know about [X]? I'll remember it."
```

## CREATOR.md Format

```markdown
# Creator Memory

## Creator
[Name], [Type of creator]. [One-sentence brand positioning.]

## Voice
**Attributes**: [3-5 voice attributes, comma-separated]
**Sounds like**: [example sentence]
**Never sounds like**: [anti-example]
**Tone rules**: [key dos and don'ts]

## Content Pillars
| Pillar | Topic focus | Core audience |
|--------|------------|---------------|
| [Pillar 1] | [What it covers] | [Who it's for] |
| [Pillar 2] | [What it covers] | [Who it's for] |
| [Pillar 3] | [What it covers] | [Who it's for] |

## Active Projects
| Project | Brief | Status |
|---------|-------|--------|
| [Name] | [1-line description] | [active/paused/upcoming] |

## Key Terms
| Term | Meaning |
|------|---------|
| [Term] | [What it means in this creator's context] |
→ Full glossary: creator-memory/voice.md

## Channels
| Channel | Tone | Key rules |
|---------|------|-----------|
| [Channel] | [Tone adaptation] | [1-2 rules] |
→ Full rules: creator-memory/channels.md

## Visual Style (quick ref)
- Aesthetic: [dark premium / light editorial / etc.]
- Primary colors: [list]
- Avoid: [list]
→ Full system: creator-memory/visual.md
```

## Building the Memory System

### First-time setup (via `/creator-sprint`)

1. Ask creator to describe their brand in 3 words
2. Probe voice with "sounds like" and "never sounds like" examples
3. Identify 3-5 content pillars
4. Document active projects
5. Ask about visual aesthetic preferences
6. Ask about music style (if relevant)
7. Create CREATOR.md and starter creator-memory/ files

### Ongoing maintenance

Update memory when:
- Creator uses a new term or phrase worth capturing
- A new project starts
- Voice or visual direction evolves
- A channel-specific rule is clarified
- A style decision is made (what worked, what didn't)

### Memory capture prompt

When you notice something worth remembering, say: "I'm saving [X] to your creator memory." Then add it to the appropriate file.

## Voice Documentation Deep-Dive

See `creator-memory/voice.md` for:
- Full voice attribute definitions with before/after examples
- Anti-patterns (what this creator never sounds like)
- Terminology glossary
- Audience profiles per channel

## Project Brief Format

```markdown
# Project: [Name]

## Brief
[3-5 sentences on what this is, who it's for, and why it matters]

## Goals
- [Goal 1]
- [Goal 2]

## Audience
[Who is this for? What do they want from it?]

## Content needed
- [Type]: [brief description]
- [Type]: [brief description]

## Status
[Active / Paused / Completed]

## Notes
[Anything else Claude needs to know]
```
