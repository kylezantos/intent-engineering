---
name: intent-engineering
description: "Ground design decisions in human needs, not abstractions. Uses a three-question framework (accomplish/notice/feel) and the Why Loop to connect every page, flow, and visual choice to bedrock intent. Two modes: Start (new project discovery) and Audit (evaluate existing site with screenshots). Use when starting a new project, designing a site, auditing a landing page, or questioning whether a design communicates the right intent."
argument-hint: "[url-or-mode]"
disable-model-invocation: true
allowed-tools: Read, Write, Edit, Glob, Grep, Bash(dev-browser *)
---

# Intent Engineering

Every design decision — words, visuals, interactions — should trace back to a human need, not to an abstraction. "We chose this because of art history" is the design equivalent of "we're the fastest way to communicate." Both are technically accurate. Neither connects.

This skill uses two techniques to ground design in real intent:

1. **The Three-Question Framework** — For each page or flow, answer: What should users accomplish? What should they explicitly notice? What should they implicitly feel?

2. **The Why Loop** — For each answer, keep asking "why does that matter?" until you hit bedrock: something universal, unique to this product, and emotional.

Inspired by Ellis Hamburger's storytelling work with Raycast, Snapchat, Daylight, Browser Company, and others.

## Quick Start

**New project:**
> `/intent-engineering start`
> `/intent-engineering` — "I'm building a new marketing site for my product"

**Audit existing site:**
> `/intent-engineering audit https://example.com`
> `/intent-engineering` — "Can you look at my landing page and tell me what it's communicating?"

---

## Core Principles

These apply to both Start and Audit workflows:

1. **Bedrock over surface** — Surface-level intent ("sign up," "look professional") isn't wrong, it's just incomplete. Drill to the human need underneath. Stop when the answer is universal, unique, and emotional.

2. **Accomplish, Notice, Feel** — Three layers that most people conflate or skip. Separating them reveals misalignment: what users notice might not lead to what you want them to feel, and what they feel might not motivate what you want them to accomplish.

3. **Mirror, don't critique** — Especially in Audit mode. Reflect what the design communicates. Ask if that matches intent. The user discovers the gaps themselves — that's more powerful than being told.

4. **Evocation over information** — A design that makes someone feel something is more effective than one that informs them of everything. Ellis: "Not trying to make the feature sound good, but first communicate that I understand you and your problem."

5. **Ideas over features** — Features are what you built. Ideas are why it matters. Ideas are more shareable, more memorable, and give you more to talk about. A product has one feature set but can own three to five ideas.

6. **Grounded, not generic** — "Be kind" is generic. "Friends over followers" is grounded. "Browse better" is generic. "The shortcut to everything" is grounded. Every principle, tagline, and design choice should be specific enough to guide a decision.

---

## Entry Point Detection

Detect mode from `$ARGUMENTS`:

| Input | Route |
|-------|-------|
| "start", "new", "building", or describes a new project | `workflows/start.md` |
| "audit", URL, "look at", "evaluate", "check my" | `workflows/audit.md` |
| Ambiguous or no arguments | Ask which mode |

If ambiguous, ask:

> I can help two ways:
> 1. **Start** — You're beginning a new project. I'll walk you through the three questions page by page to build a grounded intent brief.
> 2. **Audit** — You have an existing site or product. I'll take screenshots, reflect what I see, and help you discover where intent and execution diverge.
>
> Which one?

**After selecting a workflow, read it and follow it exactly.**

---

## The Three-Question Framework

For any page, flow, or key moment:

| Question | Layer | What it reveals |
|----------|-------|----------------|
| What should users **accomplish**? | Action | The functional outcome — what they do |
| What should they **explicitly notice**? | Attention | The conscious focus — what stands out |
| What should they **implicitly feel**? | Emotion | The unconscious response — how it lands |

Each answer gets drilled with the Why Loop until it reaches bedrock.

**The connection check:** After answering all three for a page:
- Does what they notice → lead to what they should feel?
- Does what they feel → motivate what they should accomplish?
- If these connections break, the design has a gap.

---

## Gotchas

- **Don't become a design critic.** This is the #1 risk. You are reflecting what a design communicates and asking if it matches intent. You are not evaluating quality. "This hero is too busy" is critique. "The hero draws attention before the headline — is that what you wanted?" is reflection.

- **Don't accept "delight" as bedrock.** "We want users to feel delighted" is Layer 1 wearing Layer 3's clothes. Push: "Delighted by what specifically? What changes in their day?"

- **Don't drill past bedrock.** If you keep asking "why" after hitting a universal human need, you'll land at "because life is short." True but useless. Stop when the answer is deeply human AND specific enough to differentiate this product.

- **Don't manufacture depth.** If the Why Loop reveals there isn't a clear human need underneath a design choice, that's a real finding. Surface it honestly rather than fabricating bedrock.

---

## Reference Index

| File | Contents | Load When |
|------|----------|-----------|
| [why-loop-technique.md](references/why-loop-technique.md) | Drilling technique, bedrock criteria, Ellis's examples, companion techniques | Both workflows — read before starting |
| [anti-patterns.md](references/anti-patterns.md) | Four ungrounded patterns: feature-first, intellectually-disconnected, generic/ego-inflated, aesthetic-only | Both workflows — read before starting |

## Workflow Index

| Workflow | Purpose |
|----------|---------|
| [start.md](workflows/start.md) | New project: guided three-question discovery, page by page, producing intent brief |
| [audit.md](workflows/audit.md) | Existing site: screenshots, Socratic reflection, gap identification |
