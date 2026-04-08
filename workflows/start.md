# Workflow: Start (New Project)

Guided discovery for a new project, page, or product. Walk through the three-question framework page by page, drill each answer with the Why Loop, and produce a grounded intent brief.

## Required Reading

Read these reference files before proceeding:
1. `references/why-loop-technique.md`
2. `references/anti-patterns.md`

---

## Step 1: Scope the Work

Understand what the user is building and how to break it down.

### Shortcut: Check $ARGUMENTS first

If the user already described their project at invocation (e.g., `/intent-engineering start — building a marketing site for a dev tool, main pages are homepage, pricing, and docs`), don't re-ask. Extract what they provided, present it back for confirmation, and skip to the page breakdown.

> Sounds like you're building **[extracted description]**. I'd work through these pages:
> 1. [Extracted page A]
> 2. [Extracted page B]
>
> Want to start with these, or adjust?

If no context was provided, ask:

> What are you building? Give me the high-level picture — is this a full product, a marketing site, an app, a single landing page?

Based on their answer, identify the key **pages or flows** that need intent engineering. For a marketing site, this might be:
- Homepage
- Product/feature page
- Pricing
- About

For an app, it might be:
- Onboarding flow
- Core workflow
- Empty states
- Settings/profile

Present the proposed breakdown:

> Based on what you described, I'd work through these pages/flows:
> 1. [Page A]
> 2. [Page B]
> 3. [Page C]
>
> Want to start with these, or adjust the list?

**Wait gate:** Confirm the page/flow list before proceeding.

---

## Step 2: Three Questions (Per Page/Flow)

For each page or flow, work through all three questions. Do them **one page at a time** — don't try to do every page at once.

### Announce the page

> Let's start with **[Page Name]**.

### Question 1: Accomplish

> When someone lands on this page, what do you want them to **accomplish**? What's the action or outcome?

Listen for functional answers ("sign up," "understand the product," "find pricing"). These are valid starting points.

**Apply the Why Loop:** Once they answer, drill once or twice:
- "Why is that the most important action here?"
- "What changes in their life or workflow after they do that?"

Stop when the answer connects to something the user genuinely cares about — not just a conversion metric.

### Question 2: Notice

> What do you want them to **explicitly notice** on this page? What should jump out?

Listen for visual or content elements ("the headline," "the demo video," "social proof"). This reveals what they think matters most.

**Apply the Why Loop:**
- "Why should that be the thing they notice first?"
- "What does noticing that set up for them?"

This often reveals misalignment — the thing they want people to notice isn't always connected to what they want them to accomplish.

### Question 3: Feel

> What do you want them to **implicitly feel** when they're on this page? Not what they think — what they feel.

This is the hardest question. Many people haven't considered it. Give them space. If they struggle, offer prompts:
- "Should they feel excited? Calm? Confident? Curious? Relieved?"
- "Think about the best version of someone experiencing this page — what's their emotional state?"

**Apply the Why Loop:**
- "Why is that the right feeling for this moment?"
- "How does that feeling serve what you want them to do next?"

### Synthesize the page

After all three questions, present a structured summary:

```
PAGE: [Name]

Accomplish: [Drilled answer — the real outcome, not the surface action]
Notice: [Drilled answer — what and why it matters]
Feel: [Drilled answer — the emotion and why it's right]

Connection check:
- Does what they notice → lead to what they should feel?
- Does what they feel → motivate what they should accomplish?
- If not, flag the gap.
```

> Here's what I'm hearing for [Page Name]. Does this feel right? Anything that surprises you or doesn't sit well?

**Wait gate:** Confirm before moving to the next page.

### Repeat for each page/flow

Move through the agreed-upon list, one at a time. Each page gets the full three-question treatment.

---

## Step 3: Cross-Page Coherence

After all pages are complete, look across the full set:

### Thread check
- Is there a consistent emotional thread across pages? (There should be)
- Does the "feel" from one page set up the "accomplish" of the next?
- Are there contradictions? (e.g., homepage promises excitement but product page feels clinical)

### Bedrock identification
- Across all the drilled answers, is there a single bedrock human need emerging?
- This is the equivalent of Raycast's "flow" or Snapchat's "deepen your relationships"
- If one emerges, name it. If not, that's a finding worth surfacing.

Present:

> Looking across all your pages, here's the thread I see:
>
> **Bedrock:** [The core human need this product/site serves]
>
> **Thread:** [How it flows from page to page]
>
> **Gaps:** [Where the thread breaks or contradicts]
>
> Does this resonate?

**Wait gate:** This is the most important confirmation point. The bedrock shapes everything downstream.

---

## Step 4: Intent Brief

Produce a structured brief the user can reference when making design decisions. This is the output artifact.

### Deriving design implications

For each page, derive 1-2 design implications directly from the drilled answers. These are not generic UX advice — they're choices that would only be right for *this* product's bedrock.

- Connect the implication to the bedrock, not to general best practices
- If the bedrock is "flow," the implication isn't "reduce clutter" — it's "every interaction should feel like it disappears into the task"
- If the bedrock is "deepen relationships," the implication isn't "add social features" — it's "every screen should feel like you're close to the people you care about"
- Use the connection check as your derivation: what notice → feel → accomplish chain does this page need, and what design direction serves that chain?

```
INTENT BRIEF: [Project Name]

Bedrock: [The core human need, one sentence]

---

[Page Name]
- Accomplish: [Grounded outcome]
- Notice: [What and why]
- Feel: [Emotion and why it's right]
- Design implication: [What this means for visual/copy/interaction choices]

[Page Name]
- Accomplish: ...
- Notice: ...
- Feel: ...
- Design implication: ...

---

Cross-page thread: [How the emotional arc flows]

Anti-patterns to avoid:
- [Specific to this project, drawn from the drilling]

Validation question: For every design choice, ask —
"Can I trace this back through accomplish/notice/feel to the bedrock?"
```

> Here's your intent brief. This is the reference document for design decisions going forward. Every visual choice, copy decision, and interaction pattern should be traceable back to these answers.

---

## Success Criteria

This workflow is complete when:
- [ ] Pages/flows identified and confirmed
- [ ] Three questions answered and drilled for each page
- [ ] Cross-page coherence checked
- [ ] Bedrock human need identified (or its absence surfaced)
- [ ] Intent brief produced and confirmed by user
