---
description: Audit any piece of content against the creator's brand voice and channel standards
argument-hint: "<content to review>"
---

# Content Review

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Evaluate content against the creator's voice standards and channel requirements. Returns a score, specific issues, and rewrite suggestions.

## Workflow

### 1. Receive Content

Accept:
- Pasted text (any format)
- A URL to review (if browser access is available)
- A file path
- A draft from `creator-memory/content/drafts.md`

If no content is provided, ask: "Paste or link the content you want me to review."

### 2. Identify Channel and Purpose

Ask (or infer from content):
- What channel is this for? (blog, LinkedIn, X, email, video script)
- Is there a target audience or content pillar this should belong to?

### 3. Load Standards

From `CREATOR.md` or `creator-memory/voice.md`:
- Voice attributes (what it should sound like)
- Anti-attributes (what it should never sound like)
- Channel-specific rules for the target channel
- Terminology guidelines (preferred and avoided terms)

### 4. Score the Content

Evaluate across 5 dimensions:

| Dimension | Score (1-5) | What to check |
|-----------|------------|---------------|
| **Voice match** | /5 | Does this sound like the creator? Apply attributes. |
| **Opener strength** | /5 | Does the first line earn the read? |
| **Format fit** | /5 | Right length, structure, and style for the channel? |
| **Clarity & specificity** | /5 | Concrete claims, actionable advice, no vague filler? |
| **CTA quality** | /5 | Single clear action, or no CTA where none is needed? |

Total: /25

**Thresholds:**
- 22-25: Publish-ready
- 18-21: Minor adjustments needed
- 13-17: Significant revision needed
- Below 13: Recommend starting from CREATOR.md voice and rewriting

### 5. Flag Specific Issues

For each issue found:
- Quote the exact passage
- Explain why it fails
- Provide a rewritten version

**Common issues to check:**
- Voice attributes missing (e.g., "should be confident but reads as hedged")
- Anti-patterns present (e.g., "uses 'guru' tone despite avoiding it in voice doc")
- Channel mismatch (e.g., "opening is too formal for LinkedIn's conversational feed")
- Weak opener (doesn't hook, starts with "I" or background instead of insight)
- Multiple CTAs competing
- Vague language where specificity is expected
- Terminology violations (using a word flagged as "never use")
- SEO gaps (if blog post — keyword missing from opener)

### 6. Deliver Review

```
## Content Review: [Title or first few words]
**Channel**: [inferred or stated]
**Pillar**: [which pillar this belongs to, or "unclear"]

### Score: [X]/25

| Dimension | Score | Notes |
|-----------|-------|-------|
| Voice match | /5 | [key finding] |
| Opener strength | /5 | [key finding] |
| Format fit | /5 | [key finding] |
| Clarity & specificity | /5 | [key finding] |
| CTA quality | /5 | [key finding] |

### Issues Found

**[Issue 1 — Severity: High/Medium/Low]**
> [Quoted passage]
Problem: [explanation]
Fix: [rewritten version]

[Repeat for each issue]

### What's Working
[2-3 specific things done well — not filler praise, specific observations]

### Recommendation
[Publish-ready / Minor edits / Significant revision] — [1-2 sentences on priority actions]
```

### 7. Offer Follow-Up

After review:
- "Want me to apply the suggested fixes and deliver a revised version?"
- "Should I adapt this for [another channel] after the revisions?"
- "Want this added to your drafts catalog once it's ready?"

## Tips

- A 20/25 is a strong piece — don't chase perfection at the cost of publishing
- Voice match is the most important dimension; everything else is adjustable
- If the opener is weak, that's the highest priority fix — it gates whether anyone reads the rest
- Be specific in feedback. "This doesn't match your voice" is not useful. "This uses qualifiers like 'I think' and 'maybe' which contradict your confident, direct attribute" is useful.
