# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~image generation` might mean Gemini 2.5 Flash Image, Midjourney, Stability AI, or any other image generation platform with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (image generation, email marketing, music generation, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Chat / Review | `~~chat` | Slack | Microsoft Teams, Discord |
| Knowledge base | `~~knowledge base` | Notion | Confluence, Obsidian |
| Design | `~~design` | Figma | Canva, Adobe Creative Cloud |
| Image generation | `~~image generation` | — (see note) | Gemini, Midjourney, Stability AI, Flux |
| Email marketing | `~~email marketing` | Resend | Mailchimp, ConvertKit, Beehiiv |
| Video generation | `~~video generation` | — | Veo 3, RunwayML, Kling |
| Music generation | `~~music generation` | — | Suno AI, Udio |
| Analytics | `~~analytics` | — | PostHog, Google Analytics, Amplitude |
| Publishing | `~~publishing` | — | Vercel, GitHub Pages, Webflow |

> **Note on image/music/video generation:** These tools are not standardized with HTTP MCP endpoints yet. Configure them via your local MCP server setup or direct API calls. See skills for tool-specific guidance.

## Customizing for your stack

1. Edit `.mcp.json` to add your preferred tools
2. Update placeholder references in skills and commands if needed
3. Add your brand voice and style system to `CREATOR.md` in your working directory (see creator-memory skill)
