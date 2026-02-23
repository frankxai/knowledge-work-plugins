---
name: content-creation
description: Voice-consistent content creation across blog posts, social media, newsletters, video scripts, and email. Applies brand voice attributes, per-channel tone rules, and content structure frameworks. Use when writing any content, adapting existing content for new channels, or building a content calendar.
---

# Content Creation

Produce content in your voice, at the right length and format for each channel.

## How this skill works

Content creation applies in two layers:
1. **Voice layer** — every piece sounds like you (loaded from `CREATOR.md` or `creator-memory/voice.md`)
2. **Format layer** — each channel has specific structure, length, and tone rules

If no voice documentation exists yet, ask the user to describe their voice or run `/creator-sprint` to build it.

## Voice Application

Before writing, load the creator's voice from `CREATOR.md`:
- Voice attributes (what they sound like, what they don't)
- Audience definition
- Preferred terminology and phrases to avoid
- Active content pillars

If `CREATOR.md` isn't present, ask: "Should I write in a neutral voice, or would you like to describe your style first?"

## Content Types and Formats

### Blog Post
- **Headline**: 50-65 characters, question or statement with clear benefit
- **Opening**: First 100 words must earn the scroll — lead with the key insight, not background
- **Structure**: Problem → Framework → Application → Next step
- **Length**: 800-2,000 words depending on topic depth
- **TL;DR**: Include in first 100 words for SEO and skimmers
- **Closing CTA**: One action, clearly stated

### Social Post (LinkedIn)
- **Opening line**: Stops the scroll — bold claim, surprising stat, or direct question
- **Body**: 3-5 short paragraphs, white space between each
- **Rhythm**: Vary sentence length. Short punches between longer explanations.
- **Length**: Under 1,300 characters for full display without "see more" truncation
- **CTA**: One question or action at the end

### Social Post (X / Twitter)
- **Lead tweet**: Under 280 chars, complete thought or strong hook
- **Thread option**: If concept needs more, suggest thread format (3-7 tweets)
- **Style**: Punchier and more direct than LinkedIn

### Email / Newsletter
- **Subject line**: Under 50 characters, specific benefit or curiosity gap
- **Preview text**: 85-100 characters, extends subject — don't repeat it
- **Opening**: First sentence hooks; assume reader has 3 seconds before they scroll past
- **Body**: Short paragraphs, bullet points for lists, one bold insight per section
- **CTA**: Single primary action; secondary links below the fold

### Video Script
- **Hook**: First 5 seconds must capture — question, claim, or visual promise
- **Structure**: Hook → Context (why this matters) → Core content → Summary → CTA
- **Pacing**: ~130 words per minute for comfortable delivery
- **Transitions**: Mark where B-roll, graphics, or cuts should appear

### Thread / Multi-part Content
- Each piece must work standalone *and* as part of the series
- Label position ("1 of 5") at the end, not the beginning
- Link back to the full series in each piece

## Channel Tone Adjustment

The voice stays consistent; tone adapts to context.

| Channel | Tone adjustment | Example shift |
|---------|----------------|---------------|
| Blog | Educational, considered, complete | Full arguments, referenced claims |
| LinkedIn | Professional, thought-provoking, personal | First-person insight, business framing |
| X/Twitter | Direct, punchy, slightly edgier | Shorter sentences, bolder statements |
| Email | Personal, warm, action-oriented | "You" framing, clear next step |
| Video script | Conversational, energetic, visual | Shorter sentences, action verbs |
| YouTube description | SEO-optimized, skimmable, keyword-rich | List format, timestamps |

See `creator-memory/channels.md` for your specific channel rules if configured.

## Content Pillar Alignment

When writing, check the active content pillars in `CREATOR.md`. Each piece should:
- Clearly belong to one primary pillar
- Reference the pillar's core argument or theme
- Link to at least one related piece if content catalog exists

## Repurposing Workflow

Turn one piece into many:
1. Start with the most complete format (usually long-form blog or video)
2. Extract 3-5 key insights as LinkedIn posts
3. Condense the core argument to a Twitter thread (5-7 tweets)
4. Strip to key takeaways for email summary
5. Generate 3 variations of the headline for testing

See `references/repurposing-templates.md` for format-specific templates.

## SEO Checklist (blog posts)

- [ ] Target keyword in title and first 100 words
- [ ] H2 subheadings as natural questions
- [ ] Meta description 150-160 characters with keyword
- [ ] Internal links to 2-3 related pieces
- [ ] FAQ section with 3-5 questions people actually search
- [ ] Alt text on all images

## Quality Check Before Delivering

1. **Voice match** — Does this sound like the creator? Apply attributes from CREATOR.md
2. **Opener strength** — Would a reader scroll past the first line?
3. **Format fit** — Is the length and structure right for this channel?
4. **Single purpose** — Is there one clear idea or one clear CTA?
5. **Specificity** — Are claims supported? Is advice actionable?
