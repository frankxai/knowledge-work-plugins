---
description: Create a complete content piece from brief to finished draft, in your voice and optimized for the target channel
argument-hint: "<topic or brief>"
---

# Create Content

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Produce a finished content piece — blog post, social post, newsletter, or video script — in the creator's voice for the specified channel.

## Workflow

### 1. Understand the Request

Accept any of:
- A topic ("write about AI music generation")
- A brief ("LinkedIn post: why I switched from Spotify to Suno for background work music")
- A repurpose request ("turn this blog post into a Twitter thread")
- A content type + angle ("newsletter: 3 things I learned from [specific experience]")

If the topic is unclear, ask one clarifying question only.

### 2. Load Voice and Channel Context

Check `CREATOR.md` for:
- Voice attributes and tone rules
- The target channel's specific rules (if channel isn't specified, ask)
- Active content pillars (assign this piece to one)
- Any relevant terminology or project context

If `CREATOR.md` doesn't exist, ask: "Should I write in a general voice, or describe your style quickly?"

If **~~knowledge base** is connected:
- Search for related published content to avoid repetition
- Check if there are existing notes or drafts on this topic

### 3. Clarify Format (if not obvious)

If channel or format isn't clear, ask one question:
"Is this for [inferred channel], or somewhere else?"

For blog posts, also ask:
- Target length? (short 500-800 / medium 1,000-1,500 / long 2,000+)
- SEO focus? (if yes, what's the target keyword?)

### 4. Write the Content

Apply the format rules for the target channel from the `content-creation` skill:
- Blog: headline, TL;DR, structured body, closing CTA
- LinkedIn: scroll-stopping opener, white space, single CTA
- X/Twitter: hook tweet + optional thread
- Email/newsletter: subject line, preview text, body, single CTA
- Video script: hook, structure, transitions marked

Apply voice attributes throughout. Check against "never sounds like" examples before delivering.

### 5. Deliver with Options

Present:
1. **Primary draft** — complete, ready to publish or review
2. **Headline variations** (if blog) — 3 options with different angles
3. **Subject line variations** (if email) — 3 options
4. **Repurpose suggestion** — how this could be adapted for 1-2 other channels

After delivering, ask:
- "Does this sound like you? Any sections to adjust?"
- "Want me to generate the [channel] version for repurposing?"

### 6. Optional: Save to Content Catalog

If `creator-memory/content/` exists, offer to add to `drafts.md`:
```markdown
## [Title] — [Date]
- Channel: [channel]
- Status: draft
- Pillar: [pillar]
- File: [optional path]
```

## Output Format

Deliver content in a clean markdown block, ready to copy. Format according to channel conventions (line breaks for LinkedIn, markdown headers for blog, etc.).

For email: separate subject line and preview text clearly above the body.

For video scripts: use action cues `[Action: ...]` and `[Cut to: ...]` inline.

## Tips

- If the request is vague, write the most useful interpretation and ask at the end — don't interrogate before writing.
- A good opener is more important than anything else. Write it last if needed.
- Specificity beats generality every time. Replace "a lot" with a number. Replace "many people" with "73% of creators."
