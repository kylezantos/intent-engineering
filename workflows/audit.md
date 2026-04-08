# Workflow: Audit (Existing Site/Product)

Evaluate an existing site or product against the three-question framework. Use screenshots to see what the user sees, reflect observations back Socratically, and help the user discover where their design's communicated intent diverges from their actual intent.

## Required Reading

Read these reference files before proceeding:
1. `references/why-loop-technique.md`
2. `references/anti-patterns.md`

---

## Step 1: Get the Target

### Shortcut: Check $ARGUMENTS first

If the user provided a URL at invocation (e.g., `/intent-engineering audit https://example.com`), don't ask for it again. Navigate to it immediately with `dev-browser` and take a homepage screenshot while asking about scope:

> I'm pulling up **[URL]** now. While that loads — are there specific pages you want to focus on, or should I work through the main ones?

If they also provided scope or intent hints (e.g., "homepage and pricing only, feels too cold"), acknowledge those and skip to Step 2.

### If no URL was provided

Ask what to audit:

> What's the site or product you want to look at? Give me a URL, or if it's a local project, point me to it.

If AskUserQuestion is available:
- **Live URL** — I'll open it in a browser and take screenshots
- **Local dev server** — I'll navigate to localhost
- **Existing screenshots** — I have screenshots to share

For a live URL or localhost, use `dev-browser` to navigate and take screenshots.

Also ask:

> Before I look at it — what pages or flows matter most to you? I can audit the whole thing, but if there's a specific page you're uncertain about, let's start there.

### What intent are you pressure-testing?

If a focus was extracted from `$ARGUMENTS` (e.g., "especially the copy," "whether my positioning comes through," "if the visual language feels right"), present it for confirmation:

> It sounds like you're most interested in whether **[extracted focus]**. I'll weight my observations toward that while still looking at the full picture. Sound right?

If no focus was provided, ask:

> Is there a specific intent you want to pressure-test? For example:
> - Whether your **copy** communicates ideas vs. just listing what you do
> - Whether your **visual language** creates the feeling you're going for
> - Whether your **positioning** or a specific **design decision** matches what it should communicate
> - Or something else entirely — this works for any decision you're questioning
>
> You can also skip this and I'll do a full holistic audit.

The focus doesn't narrow the audit to one dimension. It tells the agent where to apply the most pressure when reflecting back what the design communicates. Every observation still connects through accomplish/notice/feel.

**Wait gate:** Confirm the target, scope, and focus before taking screenshots.

---

## Step 2: Screenshot and Observe

For each page in scope:

1. **Navigate to the page** — use `dev-browser` to open the URL. If `dev-browser` is not available, ask the user to provide screenshots or share their screen.
2. **Take a full-page screenshot** — capture what a real user would see
3. **Observe silently first** — before sharing anything, form your own read of the page

### What to observe (internal notes, not shared yet)

For each page, note:
- **What draws the eye first?** (Visual hierarchy — what's loudest?)
- **What action does the page seem to want you to take?** (CTAs, layout flow)
- **What's the emotional tone?** (Warm? Clinical? Energetic? Sparse? Overwhelming?)
- **What story is the page telling?** (Problem → solution? Feature list? Vibes?)
- **What's missing?** (Is there a clear "why" or just a "what"?)

**If the user stated a focus**, deepen your observations in that dimension:
- **Copy/messaging**: Read every headline, subhead, and body block. Does the language communicate ideas or list capabilities? Does it complete "so that you can ___"? Does it sound like how a real person would describe this to a friend, or like marketing-speak?
- **Visual language**: What feeling does the visual treatment create independent of the words? Does the color, typography, spacing, and imagery serve an intent or just look good?
- **Positioning/product**: What does a first-time visitor understand about what this is and why it matters within 5 seconds? Is the positioning grounded in a human need or a comparison?
- **Specific decision**: Observe the specific element or choice the user asked about. What is it communicating? What feeling does it create? What action does it imply?

The focus weights your attention — it doesn't narrow the audit. Still observe the full page.

Do NOT evaluate quality. Do NOT identify design problems. You are forming a read of what the page communicates — that's different from whether it's "good."

---

## Step 3: Reflect Back (Socratic)

This is the core of the audit. You are a mirror, not a critic.

### Present your read

For each page, share what you observed — as observations, not judgments:

> Looking at **[Page Name]**, here's what I'm picking up:
>
> **First thing I notice:** [What draws the eye — could be a headline, an image, a color block, whitespace]
>
> **The action it seems to want me to take:** [What the page is pushing toward — sign up, scroll, click, read]
>
> **The feeling I get:** [The emotional tone — be specific and honest. "Professional but distant." "Energetic but unfocused." "Calm and confident."]
>
> **The story it's telling:** [What narrative structure, if any. "Here's what we do, here's how it works, here's social proof." Or "Here's a vibe, no clear next step."]

### Then ask — don't tell

> **Is that what you intended?**

That single question does most of the work. Let the user respond. They'll either:
- **Confirm** — "Yeah, that's exactly right" → move to next page
- **Partially confirm** — "The feeling is right but the action isn't clear enough" → drill into the gap
- **Disagree** — "No, I wanted them to feel X not Y" → now you've found the divergence

### If there's a gap

When the user's intent doesn't match what the page communicates, don't prescribe a fix. Instead, drill:

> You wanted them to feel [X], but the page is giving off [Y]. Let's figure out why.
>
> - What on this page do you think is creating the [Y] feeling?
> - What would need to change for [X] to come through instead?
> - Is [X] still the right target, or has your thinking shifted?

Use the Why Loop here — if the user says "I want them to feel inspired," ask "Why is inspired the right feeling for this moment? What does it set up?"

### Connect to anti-patterns

When a gap emerges, check whether an anti-pattern from `references/anti-patterns.md` is at play — but surface it through the user's language, not as a label:

- If the page leads with what rather than why → may be **feature-first**. Surface specific text: "This line says [X] — is that the idea you want to lead with, or is there a deeper 'so that you can' underneath it?"
- If the design reasoning won't land with the audience → may be **intellectually-disconnected**. Ask: "This choice makes sense to me — would your [audience] connect with it the same way?"
- If the language could apply to anyone → may be **generic/ego-inflated**. Ask: "Could a competitor paste this exact line on their site? What makes this specifically yours?"
- If a visual or structural choice looks good but doesn't serve accomplish/notice/feel → may be **aesthetic-only**. Ask: "This is visually strong — what intent is it serving?"

**If the user stated a focus**, prioritize anti-pattern checks in that dimension. But surface whatever you actually observe — the focus is a weight, not a filter.

---

## Step 4: Three-Question Assessment

After the Socratic reflection, structure what you've learned using the framework.

For each audited page:

```
PAGE: [Name]

What you intended:
- Accomplish: [What the user told you]
- Notice: [What they wanted highlighted]
- Feel: [Target emotion]

What the page communicates:
- Accomplish: [What the page actually pushes toward]
- Notice: [What actually draws attention]
- Feel: [Actual emotional tone from the screenshot]

Alignment:
- Accomplish: [Aligned / Partially aligned / Misaligned] — [brief note]
- Notice: [Aligned / Partially aligned / Misaligned] — [brief note]
- Feel: [Aligned / Partially aligned / Misaligned] — [brief note]
```

### Identify patterns

If you audited multiple pages, look for recurring patterns:

- Is misalignment concentrated in one dimension? (e.g., "accomplish" is always clear but "feel" is consistently off)
- Is there an anti-pattern at work? (Feature-first? Aesthetic-only? Intellectually-grounded-but-disconnected?)
- Is the cross-page thread coherent or fragmented?

**Use anti-pattern labels internally to guide your thinking, but present findings through the user's own language.** Don't say "this is feature-first." Say "the page leads with what the product does rather than why it matters — is that intentional?"

---

## Step 5: Gap Prioritization

Help the user decide what to address:

> Here are the gaps I see, in order of impact:
>
> 1. **[Biggest gap]** — [Which page, which dimension, what the divergence is]
> 2. **[Second gap]** — ...
> 3. **[Third gap]** — ...
>
> Which of these feel most urgent to you?

If AskUserQuestion is available, present the top 3 gaps as selectable options.

**Do not propose design solutions.** This skill identifies where intent and execution diverge. The user (or another skill/process) handles the fix. You can suggest what the design should *aim for* — but not how to get there visually.

The one exception: if the user explicitly asks "what would you change?" — then you can offer directional suggestions framed as hypotheses, not prescriptions:
- "One hypothesis: if the headline led with the problem instead of the feature, the 'accomplish' alignment might improve."
- "You might explore whether a warmer color palette shifts the feeling from 'clinical' toward 'confident.'"

---

## Gotchas

- **Don't slip into critique mode.** This is the #1 failure risk. You are not evaluating whether the design is good. You're reflecting what it communicates and asking if that matches intent. "This hero image is too busy" is critique. "The hero image draws attention before the headline — is that what you wanted?" is reflection.

- **Don't project intent the user hasn't stated.** If you observe something on the page, reflect it as observation. Don't say "it seems like you wanted X" unless the user told you they wanted X. Say "I'm picking up X from this page" and let them confirm or deny.

- **Don't evaluate copy in isolation.** This skill looks at what the page communicates holistically — copy, visuals, layout, hierarchy working together. Don't pull out a headline and critique it separately. Everything is in service of accomplish/notice/feel.

- **Don't skip the screenshot.** Reading code or markup is not the same as seeing the page. The user experiences their product visually. You need to see what they see. Always take screenshots before reflecting.

- **Don't overwhelm with observations.** Three to four observations per page is plenty. First thing noticed, implied action, emotional tone, story structure. More than that and you're writing a report, not having a conversation.

- **Don't rush past "is that what you intended?"** That question is where the real work happens. Sit in the silence. Don't immediately follow it with your own analysis. Let the user respond first.

---

## Success Criteria

This workflow is complete when:
- [ ] Target site/product identified and scoped
- [ ] Screenshots taken for each page in scope
- [ ] Observations reflected back Socratically for each page
- [ ] User confirmed or identified gaps for each page
- [ ] Three-question assessment structured for each page
- [ ] Gaps prioritized by impact
- [ ] User has clarity on where intent and execution diverge
