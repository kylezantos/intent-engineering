# Intent Engineering

A Claude Code skill that helps you ground design decisions in human needs — not abstractions, not feature lists, not aesthetic preferences.

## The Problem

Most design decisions start (and stop) at the surface:

- **"We need a bold hero section"** — Why? What should it make someone feel?
- **"Our product is the fastest way to ___"** — So what? Why does that matter to a human being?
- **"We chose this visual language because it references Bauhaus"** — Cool, but your users don't know Bauhaus. What are they supposed to feel?

These decisions aren't wrong — they're just incomplete. They describe *what* without connecting to *why it matters*. And when you can't trace a design choice back to a real human need, you can't evaluate whether it's working.

## The Technique

Intent Engineering combines two ideas:

### The Why Loop

Borrowed from Ellis Hamburger's storytelling work with startups like Raycast, Snapchat, the Browser Company, and Daylight. When founders describe their product, Ellis keeps asking **"why does that matter?"** until he hits bedrock — the fundamental human need underneath the features.

**Example (Raycast):**
- "You don't have to switch apps" → *why?*
- "You're not getting distracted" → *why?*
- "You can stay in flow" → **Bedrock. "The shortcut to everything."**

**Example (Snapchat):**
- "It's the fastest way to communicate" → *so that you can...?*
- "Share moments from your day" → *why?*
- "Your friends feel like they're there with you" → **Bedrock. "Deepen your relationships with the people that matter most."**

Ellis used this for branding and copy. This skill extends it to design decisions and visual language.

### The Three-Question Framework

For any page, flow, or key moment in a product, answer three questions:

1. **What should users accomplish?** — The functional outcome
2. **What should they explicitly notice?** — What draws conscious attention
3. **What should they implicitly feel?** — The emotional undercurrent

Then apply the Why Loop to each answer until you hit bedrock. The magic is in the connection check: does what they *notice* lead to what they should *feel*? Does what they *feel* motivate what they should *accomplish*? When those connections break, you've found a design gap.

## Two Modes

### Start — New Project Discovery

Walk through the three questions page by page for a new project. Drill each answer. Produce an intent brief that grounds every design decision in human need.

```
/intent-engineering start
```

### Audit — Existing Site Evaluation

Take screenshots of an existing site, reflect back what the design communicates (visual hierarchy, emotional tone, implied action), and ask: **"Is that what you intended?"**

The audit mode is Socratic, not critical. It doesn't tell you your design is bad — it mirrors what your design is *saying* and lets you discover whether that matches what you *meant*.

```
/intent-engineering audit https://your-site.com
```

## Installation

Copy the `intent-engineering` directory to your Claude Code skills folder:

```
~/.claude/skills/intent-engineering/
```

Then invoke with `/intent-engineering` in any Claude Code session.

## Origin

Synthesized from [Ellis Hamburger's Dive Club episode on startup storytelling](https://www.youtube.com/watch?v=jrMjbdHNg4E) and extended into product design by Kyle Zantos. Built with [skill-distillery](https://github.com/kylezantos/skill-distillery).
