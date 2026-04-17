# AI Patterns for Product Development

Real-world patterns for using AI agents in product development, extracted from building [Superproper](https://superproper.co) — a B2B SaaS for real estate agents.

**This is not theory.** Every pattern here runs in production. 300+ user feedbacks managed, 60+ shipped, zero dedicated PM.

## The Core Idea

Most product teams collect user feedback. Few manage it well. The sorting, cross-referencing, prioritizing, and — most importantly — closing the loop back to the user is tedious bookkeeping that everyone abandons after 3 weeks.

AI agents don't abandon bookkeeping. They do it every time, for near-zero cost.

This repo documents the patterns that make this work.

## What's Here

### Diagram
**[AI-Powered Feedback Loop](https://hugoblanc.github.io/feedback-flow/)** — Visual walkthrough of the complete pipeline from Slack message to customer notification.

### Patterns (coming soon)
| Pattern | Description |
|---------|------------|
| Feedback Ingestion | Auto-classify feedback into a structured markdown tree |
| Feedback Refinement | Impact × complexity evaluation with GO / DISCUSS / REJECT |
| Closed-Loop Notification | Post back in the original Slack thread when shipped |
| Skill Chaining | How skills compose into complete workflows |
| Written Culture as AI Leverage | Why text-heavy teams win with AI agents |

See [TOPICS.md](TOPICS.md) for the full backlog.

### Posts
- [2026-04-16 — LinkedIn FR: ProductBoard vs AI Agents](posts/2026-04-16-linkedin-feedback-loop-fr.md)

## Inspired By

- [Andrej Karpathy — LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) — Persistent, LLM-maintained knowledge bases
- [Claude Code](https://claude.ai/claude-code) — AI coding tool powering the agent workflows

## About

Built by [Hugo Blanc](https://www.linkedin.com/in/hugoblanc/) — CTO at Superproper, building AI-powered tools for real estate professionals.
