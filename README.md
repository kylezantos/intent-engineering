# Intent Engineering

A Claude Code skill that grounds design decisions in human needs — not abstractions, not feature lists, not aesthetic preferences.

## What It Does

Most design decisions start (and stop) at the surface:

- **"We need a bold hero section"** — Why? What should it make someone feel?
- **"Our product is the fastest way to ___"** — So what? Why does that matter to a human being?
- **"We chose this visual language because it references Bauhaus"** — Cool, but your users don't know Bauhaus. What are they supposed to feel?

These decisions aren't wrong — they're incomplete. They describe *what* without connecting to *why it matters*. When you can't trace a design choice back to a real human need, you can't evaluate whether it's working.

Intent Engineering helps you find that connection using two techniques:

### The Why Loop

Keep asking **"why does that matter?"** until you hit bedrock — the fundamental human need underneath the features.

**Example (Raycast):**
- "You don't have to switch apps" → *why does that matter?*
- "You're not getting distracted" → *why does that matter?*
- "You can stay in flow" → **Bedrock: "The shortcut to everything."**

**Example (Snapchat):**
- "It's the fastest way to communicate" → *so that you can...?*
- "Share moments from your day" → *why does that matter?*
- "Your friends feel like they're there with you" → **Bedrock: "Deepen your relationships with the people that matter most."**

### The Three-Question Framework

For any page, flow, or key moment in a product, answer three questions:

1. **What should users accomplish?** — The functional outcome
2. **What should they explicitly notice?** — What draws conscious attention
3. **What should they implicitly feel?** — The emotional undercurrent

Then apply the Why Loop to each answer. The connection check is where it gets interesting: does what they *notice* lead to what they should *feel*? Does what they *feel* motivate what they should *accomplish*? When those connections break, you've found a design gap.

## Two Modes

### Start — New Project Discovery

Walk through the three questions page by page for a new project. Drill each answer with the Why Loop. Produce an intent brief that grounds every design decision in human need.

```
/intent-engineering start
```

### Audit — Existing Site/Product Evaluation

Take screenshots of an existing site, reflect back what the design communicates, and ask: **"Is that what you intended?"**

The audit is Socratic, not critical. It doesn't tell you your design is bad — it mirrors what your design is *saying* and lets you discover whether that matches what you *meant*.

```
/intent-engineering audit https://your-site.com
```

You can focus the audit on what you're most uncertain about — your copy, visual language, product positioning, a specific design decision — and the skill will weight its observations toward that while still looking at the full picture.

## Use Cases

- **Landing page copy audit** — "Does my headline communicate an idea or just list what I do?"
- **Portfolio review** — "Does my site communicate who I am and what I care about, or just show work?"
- **Product positioning** — "Can a first-time visitor understand why this matters in 5 seconds?"
- **Visual language check** — "Does the visual tone match the feeling I want to create?"
- **New project kickoff** — "Before I design anything, what should each page make someone accomplish, notice, and feel?"
- **Design decision validation** — "I chose this direction — can I trace it back to a human need?"

## What It's Not

This isn't a UI audit tool. It doesn't evaluate visual quality, accessibility, or usability. It's about **intent alignment** — whether what your design communicates matches what it should communicate. The output is clarity about where intent and execution diverge, not a list of design fixes.

## Install

### One command (all agents)

```bash
npx skills add kylezantos/intent-engineering
```

Auto-detects your installed agents and installs to each. Works with Claude Code, Codex, OpenCode, Cursor, Gemini CLI, Windsurf, and [35+ more](https://github.com/vercel-labs/skills).

### Target specific agents

```bash
npx skills add kylezantos/intent-engineering -a claude-code
npx skills add kylezantos/intent-engineering -a codex -a opencode
```

### Manual install

Copy the entire `intent-engineering/` directory into your agent's skills path:

| Agent | Path |
|-------|------|
| Claude Code | `~/.claude/skills/intent-engineering/` |
| Codex | `~/.codex/skills/intent-engineering/` |
| OpenCode | `~/.config/opencode/skills/intent-engineering/` |
| Cursor | `~/.cursor/skills/intent-engineering/` |
| Gemini CLI | `~/.gemini/skills/intent-engineering/` |
| Windsurf | `~/.codeium/windsurf/skills/intent-engineering/` |

Or clone:

```bash
git clone https://github.com/kylezantos/intent-engineering.git ~/.claude/skills/intent-engineering
```

Then invoke with `/intent-engineering` in any session.

**Cross-agent compatibility:** The core workflow (three questions, Why Loop, Socratic reflection) works on any AI coding agent. Claude Code users get enhanced features like tappable options and automated screenshots via `dev-browser`.

## Origin

Synthesized from [Ellis Hamburger's Dive Club episode on startup storytelling](https://www.youtube.com/watch?v=jrMjbdHNg4E) and extended into product design. Built with [skill-distillery](https://github.com/kylezantos/skill-distillery).
