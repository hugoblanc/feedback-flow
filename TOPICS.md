# Topics Backlog

Topics to cover in this repository. Checked items are published, unchecked are planned.

## Patterns

### Feedback Management
- [ ] **Feedback Ingestion** — Auto-classifying user feedback from Slack/Chatwoot into a structured markdown tree organized by product domain. How the agent reads threads, picks the right branch, creates the file with frontmatter, and reacts on Slack.
- [ ] **Feedback Refinement** — Automated impact × complexity evaluation. The GO / DISCUSS / REJECT matrix. How the agent posts in #product-refinement when human input is needed, tags the right people, and updates frontmatter.
- [ ] **Closed-Loop Notification** — The `/done` skill: when dev is finished, the agent posts back in the original Slack thread, marks feedback as done, closes the Linear ticket. Why this is the hardest part to do manually and the most impactful to automate.
- [ ] **Feedback-to-Dev Pipeline** — The full end-to-end: from a Slack message to deployed code. How ingestion, refinement, dev, and closed-loop chain together via skills.

### Skill Architecture
- [ ] **Skill Chaining** — How skills (`/project-management`, `/refine`, `/done`) trigger and complement each other to form complete workflows. The SKILL.md format and how to design skills that compose well.
- [ ] **Skill Design Principles** — What makes a good skill vs a bad one. Scope, triggers, idempotency, error handling. Lessons learned from building 15+ skills.

### AI Agent Workflows
- [ ] **Agent-Powered Bug Fixing** — Spawning an autonomous agent on a Linear issue. How it reads the ticket, explores the codebase, writes the fix, runs tests, and creates a PR. When it works, when it doesn't.
- [ ] **LLM as Bookkeeper** — The Karpathy "LLM Wiki" pattern applied to product management. Why LLMs excel at the tedious maintenance work humans abandon. Cross-referencing, deduplication, status tracking.
- [ ] **MCP as the Integration Layer** — How Model Context Protocol replaces traditional SaaS integrations. Slack, Chatwoot, Linear, databases — all through a single protocol. Why this matters for the "SaaS crisis."

### Product & Process
- [ ] **Written Culture as AI Leverage** — Why companies with strong written communication habits will be massively advantaged. Every Slack thread, every structured discussion = exploitable context for AI agents. Text is gold.
- [ ] **The SaaS Unbundling** — Cloning the 20% of a $800/month tool you actually use. When it makes sense, when it doesn't. The honest cost breakdown (setup time + API cents vs subscription).
- [ ] **Feedback-Driven Development at Startup Scale** — Running product management without a dedicated PM. How a solo CTO uses AI agents to maintain the feedback loop that teams of 5 struggle with.

### Technical Deep-Dives
- [ ] **Markdown as Database** — Why a git repo of markdown files with YAML frontmatter beats a database for feedback tracking at small scale. Grep, git blame, PR reviews on feedbacks.
- [ ] **Slack as Product Hub** — How Slack becomes the central nervous system when AI agents can read, react, and post. The emoji protocol (💾 = ingested, ⏳ = in progress, ✅ = shipped).

## Posts (Published)
- [x] **2026-04-16 — LinkedIn FR: ProductBoard vs AI Agents** — Feedback loop automation, Karpathy reference, SaaS crisis angle. [Post](posts/2026-04-16-linkedin-feedback-loop-fr.md) | [Diagram](index.html)

## Future Content Ideas (not yet scoped)
- Speech-to-text as input layer for feedback (dictate instead of type)
- AI-powered product refinement meetings (agent prepares, facilitates, summarizes)
- Monitoring agent quality: how to know when the agent gets it wrong
- The role of CLAUDE.md as "organizational memory" for AI agents
- Building in public with AI: what to share, what to keep private
