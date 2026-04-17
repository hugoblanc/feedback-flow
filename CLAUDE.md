# AI Patterns — Repository Guidelines

This repository documents real-world patterns for using AI agents in product development, based on hands-on experience building [Superproper](https://superproper.co), a B2B SaaS for real estate agents.

## Purpose

Personal branding + knowledge sharing. Each piece of content is grounded in actual production usage, not theory. The goal is to build a rich, referenceable base of AI-powered product development patterns over time.

## Language

- **Default language: English** for all documentation, README, patterns, and articles.
- **Exception**: LinkedIn posts or content explicitly targeting a French audience may be written in French. These should be stored in locale-specific folders or clearly marked (e.g., `posts/2026-04-16-linkedin-fr.md`).
- The `index.html` diagram is in French (LinkedIn post asset) — this is intentional.

## Content Types

### 1. Patterns (`patterns/`)
Short, actionable articles (500-800 words) documenting a specific AI-powered workflow pattern.

**Structure for each pattern:**
- **Problem** — What sucks without it. Be concrete, not abstract.
- **Pattern** — How it works. The mechanism, not the tool.
- **Implementation** — Concrete example from Superproper (or similar real case). Include file structures, code snippets, actual Slack messages when relevant.
- **When to use / When not to use** — Honest boundaries. Don't oversell.

**Naming**: `kebab-case.md` (e.g., `feedback-ingestion.md`, `closed-loop-notification.md`)

### 2. Posts (`posts/`)
Archive of published content (LinkedIn, blog, etc.) for reference. These are snapshots — don't edit after publishing.

**Naming**: `YYYY-MM-DD-platform-topic.md` (e.g., `2026-04-16-linkedin-feedback-loop-fr.md`)

### 3. Visual Assets (`assets/`)
Diagrams, screenshots, HTML pages used in posts. The `index.html` at root is a special case (GitHub Pages entry point for the feedback flow diagram).

## Writing Style

### Tone
- **Builder tone**, not thought leader tone. "I built this, here's what I learned" > "Here are 10 tips for..."
- Direct, concise. Short sentences. Cut filler words.
- Tech-savvy audience assumed: CTOs, senior devs, product managers, CPOs at startups/scale-ups.
- Assume deep technical knowledge. Skip basic explanations.
- Opinions are welcome and should be clearly owned ("I think...", "In my experience...").
- Light humor OK, no corporate jargon, no buzzwords.

### Honesty & Nuance
- **Never oversell**. If something only works at startup scale, say it. If there are limitations, acknowledge them.
- Include disclaimers when comparing to established tools (ProductBoard, Linear, etc.) — we're not claiming to replace them, we cloned the part we needed.
- Anticipate counterarguments. Address them proactively rather than ignoring them.
- "For zero cost" is dishonest — say "setup time + a few cents of API" instead.

### Formatting
- GitHub-flavored Markdown.
- Use code blocks for file structures, configs, CLI commands.
- Use real examples (anonymize if needed, but keep them concrete).
- No emojis in articles/patterns. Emojis are acceptable in LinkedIn posts only, and sparingly.
- Headers: `#` for title, `##` for sections, `###` for subsections. Don't go deeper than `###`.

## Key Concepts to Reference

These are the building blocks that patterns are built on. Use consistent terminology:

- **Skill** — A structured prompt file (SKILL.md) that gives an AI agent specialized capabilities and workflow instructions. Like a runbook, but for an AI.
- **MCP (Model Context Protocol)** — Open protocol for connecting AI agents to external tools (Slack, databases, APIs). The "USB-C of AI integrations."
- **Feedback loop** — The complete cycle: user reports issue → feedback ingested → refined → developed → shipped → user notified.
- **Closed loop** — The critical last step: notifying back in the original thread/channel where the feedback originated.
- **Bookkeeping** — The tedious maintenance work (sorting, cross-referencing, prioritizing, updating statuses) that humans abandon but LLMs handle effortlessly. Term borrowed from Karpathy's LLM Wiki post.
- **Refinement** — Automated evaluation of a feedback's impact × complexity to decide GO / DISCUSS / REJECT before development.

## References

- [Andrej Karpathy — LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) — The conceptual foundation for persistent, LLM-maintained knowledge bases.
- [Superproper](https://superproper.co) — The B2B SaaS where these patterns are battle-tested.
- [Claude Code](https://claude.ai/claude-code) — The AI coding tool powering the agent workflows.

## Repository Structure

```
feedback-flow/
├── CLAUDE.md                      # This file — repo guidelines
├── README.md                      # Public-facing intro + table of contents
├── index.html                     # LinkedIn diagram (FR) — GitHub Pages
├── og-image.png                   # Social preview image
├── TOPICS.md                      # Backlog of topics to cover
├── patterns/
│   ├── feedback-ingestion.md
│   ├── feedback-refinement.md
│   ├── closed-loop-notification.md
│   ├── skill-chaining.md
│   └── ...
├── posts/
│   ├── 2026-04-16-linkedin-feedback-loop-fr.md
│   └── ...
└── assets/
    └── ...
```

## When Adding Content

1. Check `TOPICS.md` to see if the topic is already listed. If so, update its status.
2. Write the content following the structure above.
3. Add an entry to the README table of contents.
4. If it's a LinkedIn post, also update `index.html` or create a new GitHub Pages asset if needed.
5. Keep patterns independent — each should be readable on its own without requiring other patterns.
