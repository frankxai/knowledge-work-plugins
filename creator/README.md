# Creator Plugin

Create content, visuals, and music — consistently, at scale, and in your voice.

This plugin is designed for independent creators, personal brands, and creative businesses who produce content across multiple formats and channels. It brings brand voice management, visual style systems, multi-channel content production, and music generation pipelines to Claude.

## What this plugin does

- **Content creation** — Write blog posts, social content, newsletters, and scripts in a consistent voice across channels
- **Visual creation** — Generate and curate images using a defined style system with quality gates
- **Music production** — Engineer prompts for AI music generation (Suno and compatible tools)
- **Creator memory** — Build and maintain a brand knowledge base so Claude works like a creative collaborator

## Getting started

### Install (Claude Code)

```bash
claude plugins add frankxai/knowledge-work-plugins/creator
```

### Initialize your creative workspace

After installing, run `/creator-sprint` to set up your workspace:
- Creates `CREATOR.md` — your brand and voice working memory
- Sets up `creator-memory/` — full brand knowledge base
- Walks you through documenting your voice, visual style, and content strategy

### Set up your tools

Edit `.mcp.json` to connect:
- `~~chat` for content review and draft sharing
- `~~knowledge base` for long-term project storage
- `~~email marketing` for newsletter distribution

See [CONNECTORS.md](./CONNECTORS.md) for the full list.

## Skills

| Skill | What it does |
|-------|-------------|
| [content-creation](./skills/content-creation/) | Voice-consistent content across blog, social, email, video |
| [visual-creation](./skills/visual-creation/) | Style-governed image generation with quality gates |
| [music-production](./skills/music-production/) | Suno prompt engineering and music pipeline |
| [creator-memory](./skills/creator-memory/) | Brand DNA, voice documentation, project catalog |

## Commands

| Command | What it does |
|---------|-------------|
| `/create-content <topic>` | Draft a content piece from brief to finished |
| `/create-visual <concept>` | Generate visual with style and quality checks |
| `/create-music <style>` | Engineer a Suno prompt and document the track |
| `/creator-sprint` | Start a focused creative session or initialize workspace |
| `/content-review <content>` | Audit any content for brand voice compliance |

## How it works with your brand

The plugin stores your brand knowledge in two places:

```
CREATOR.md           ← Working memory (voice, style, active projects)
creator-memory/
  voice.md           ← Brand voice attributes and tone rules
  visual.md          ← Visual style DNA and generation settings
  music.md           ← Music style and Suno prompt patterns
  channels.md        ← Per-channel content rules
  projects/          ← Project briefs and content catalogs
```

The creator-memory skill builds and maintains this system. The more context you give Claude, the more consistently it writes in your voice and style.

## Making it yours

This plugin becomes most powerful when you:

1. Run `/creator-sprint` to initialize your brand knowledge base
2. Document your voice attributes (what you sound like, what you don't)
3. Define your visual style (colors, mood, composition rules)
4. Set per-channel rules (tone adjustments for LinkedIn vs. blog vs. email)

See [cowork-plugin-management](../cowork-plugin-management/) for how to customize plugins further.

---

*Built on ACOS (Agentic Creator OS) patterns by [FrankX AI](https://frankx.ai).*
