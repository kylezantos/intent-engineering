# Anti-Patterns: Ungrounded Design Decisions

How to recognize design decisions that aren't rooted in human need. Used in both Start (prevention) and Audit (diagnosis) workflows.

## The Four Ungrounded Patterns

Every ungrounded design decision falls into one of these categories. Learn to recognize them — in your own work and in what you're evaluating.

### 1. Feature-First

The design communicates what the product does, not why it matters.

**Signs:**
- Headlines like "faster," "better," "more efficient," "all-in-one"
- Visual hierarchy organized by feature list rather than user story
- Onboarding that tours features instead of priming expectations
- Pages that read like a spec sheet

**Why it fails:** Features aren't unique. "Browse better" sounds simple but has no meaning — every browser could say it. It's not a hook because it doesn't connect to a feeling or a problem.

**The fix:** Apply the Why Loop. "We have X feature" → "so that you can ___" → keep going until you hit a human need that only you can credibly own.

**Ellis's example:** Snapchat was stuck on "the fastest way to communicate" for years. Functional, true, but meaningless — texting is pretty fast too. It took asking "so that you can ___?" to arrive at "deepen your relationships with the people that matter most."

### 2. Intellectually-Grounded-But-Disconnected

The design is rooted in a real idea, but one the audience won't connect with.

**Signs:**
- Visual language explained through art movements, philosophy, or theory
- Design rationale that requires domain expertise to appreciate
- Choices that are internally coherent but externally opaque
- "We chose this because of [reference most users don't know]"

**Why it fails:** The reasoning is real, but it lives in the designer's head, not the user's experience. A visual language rooted in Bauhaus means nothing to someone who doesn't know Bauhaus. The design might still work accidentally — but you can't evaluate or iterate on reasoning your audience doesn't share.

**The fix:** Translate the intellectual grounding into the three questions:
- What should users **accomplish** on this page? (Does the art-history choice serve that?)
- What should they **explicitly notice**? (Does the reference communicate what you think it does?)
- What should they **implicitly feel**? (Is the feeling accessible without knowing the reference?)

If the design works through the three questions independent of its intellectual backstory, it's fine — the backstory is just bonus context. If it only works when you know the backstory, it's disconnected.

### 3. Generic / Ego-Inflated

The design communicates importance without specificity, or inflates value beyond what's credible.

**Signs:**
- Mission statements like "contribute to human progress"
- Values like "be kind," "move fast," "innovate"
- Language that sounds impressive but could apply to any company
- Silicon Valley jargon: "leverage," "empower," "disrupt," "reimagine"
- Visuals designed to impress rather than communicate

**Why it fails:** Generic statements don't guide decisions. "Be kind" doesn't tell a designer what to build. "Contribute to human progress" doesn't tell a salesperson what to pitch. And inflated language triggers the bullshit radar — as Ellis puts it, "who talks about pitching their friend like 'oh yeah this tool is such a good way to leverage your blah blah blah'?"

**The fix:** Make it specific and actionable. Ellis's examples of good principles:
- "Simple apps over super apps" (Amo)
- "Friends over followers" (Snapchat)
- "Hesitate before gamifying"

These are opinionated, memorable, and they actually help someone make a decision when they're stuck.

### 4. Aesthetic-Only

The design looks good but isn't in service of anything.

**Signs:**
- Visual choices justified by "it looks nice" or "it's trendy"
- Typography, color, and layout decisions made in isolation from intent
- Beautiful design that doesn't communicate what the user should do, notice, or feel
- Style that could belong to any product in the category

**Why it fails:** Aesthetic quality is necessary but not sufficient. A beautiful page that doesn't communicate intent is decoration, not design. And decoration is indistinguishable from every other well-designed product.

**The fix:** Run the three-question test. For each major visual choice:
- Does this help the user accomplish what they came here to do?
- Does this draw their attention to the right thing?
- Does this make them feel what you want them to feel?

If a visual choice serves at least one of these — great, keep it. If it serves none, it's aesthetic-only and should be reconsidered.

## Using This in Audit Mode

When auditing an existing site, don't lead with "this is feature-first" or "this is ungrounded." Instead, use Socratic reflection:

1. Describe what you observe on the page — what draws attention, what the hierarchy communicates, what the emotional tone feels like
2. Ask the user: "Is that what you intended?"
3. If there's a gap, help them identify which pattern is at play
4. Use the Why Loop to find what the design should be rooted in instead

The anti-pattern labels are diagnostic tools for you, not critiques to present to the user.

## Using This in Start Mode

When building from scratch, use these patterns as guardrails:

- After the user answers the three questions, check: are any answers feature-first? Drill deeper.
- When they describe visual direction, check: is it intellectually grounded but disconnected? Translate through the three questions.
- When they articulate mission/values, check: are they generic? Push for specificity and actionability.
- When they describe aesthetics, check: are they in service of intent? Connect each choice to accomplish/notice/feel.
