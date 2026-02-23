---
description: Start a focused creative work session, or initialize the creator workspace for the first time
---

# Creator Sprint

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Start a focused creative session or set up the creator workspace from scratch.

## Workflow

### Detect Mode

First, check if `CREATOR.md` exists in the working directory.

- **Exists** → sprint mode (daily session start)
- **Doesn't exist** → initialization mode (first-time setup)

---

## Initialization Mode (First Run)

Build the creator's brand knowledge base from scratch.

### Step 1: Creator Profile

Ask conversationally — don't dump all questions at once:

"Let's set up your creator workspace. A few quick questions to start:
1. What type of creator are you? (content, music, products, personal brand, etc.)
2. What's your core audience — who do you make things for?
3. What's your brand in 3 words?"

### Step 2: Voice Documentation

"Now let's capture your voice — this is what I'll use every time I write for you.

Give me an example of something you've written that sounds exactly like you. And one example of content that's in your category but sounds nothing like you."

From these examples, extract:
- 3-5 voice attributes (what it sounds like)
- 3-5 anti-attributes (what it never sounds like)
- Recurring phrases or sentence structures
- Tone preference by channel if different

### Step 3: Content Pillars

"What are the main topics or themes you create content about? Give me 3-5 pillars."

For each: name, brief description, core audience.

### Step 4: Visual Style (optional)

"Do you have an established visual aesthetic? Describe it, or share an example image."

Capture: aesthetic direction, colors, mood, what to avoid.

### Step 5: Music (optional)

"Do you create or use music in your work? If so, what's your sound?"

Capture: genre preferences, use cases, any existing style anchors.

### Step 6: Active Projects

"What are you actively working on right now? Give me a name and one-line brief for each."

### Step 7: Create Files

Generate:
1. `CREATOR.md` — working memory (voice, pillars, projects, quick-ref)
2. `creator-memory/voice.md` — full voice documentation with examples
3. `creator-memory/channels.md` — per-channel rules (if multiple channels discussed)
4. `creator-memory/visual.md` — visual style (if discussed)
5. `creator-memory/music.md` — music style (if discussed)
6. `creator-memory/projects/` — one file per active project

### Step 8: Completion Report

```
✓ Creator workspace initialized

Files created:
• CREATOR.md — working memory (covers ~90% of daily requests)
• creator-memory/voice.md — full voice documentation
• creator-memory/channels.md — channel-specific rules
[• creator-memory/visual.md — visual style system]
[• creator-memory/music.md — music production anchors]
[• creator-memory/projects/]

Ready to:
• /create-content — write anything in your voice
• /create-visual — generate on-brand images
• /create-music — engineer music prompts
• /content-review — check content against your standards
```

---

## Sprint Mode (Daily Session)

Start a focused creative session.

### Step 1: Load Context

Read `CREATOR.md`:
- Current content pillars
- Active projects and their status
- Any notes from last session (if logged)

If **~~knowledge base** is connected, check for recent notes or drafts.

### Step 2: Session Orientation

Display a brief orientation:

```
Ready to create. Here's your current context:

Active projects:
• [Project 1] — [status]
• [Project 2] — [status]

Suggested focus today:
• [Based on context/recency — what seems most pressing]

What do you want to create?
```

### Step 3: Create

Execute whatever the creator requests. Common sprint tasks:
- Content creation (`/create-content`)
- Visual prompt engineering (`/create-visual`)
- Music production (`/create-music`)
- Content review (`/content-review`)
- Project brief (`/project-brief`)

### Step 4: End-of-Session Log (optional)

After each sprint, offer to update project status in CREATOR.md:
"Want to log what we created today to keep your workspace current?"

Update relevant project statuses and add new terminology or style decisions captured during the session.

## Tips

- Run `/creator-sprint` at the start of each session to orient Claude to your current work
- Update CREATOR.md whenever a new project starts or a key creative decision is made
- The more specific your voice documentation, the less explanation you need to give per piece
