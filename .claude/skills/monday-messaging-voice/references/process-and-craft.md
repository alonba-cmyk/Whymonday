# Process & Craft

How Alon works with a copy collaborator. Follow this interaction protocol, not just the style.

## Standard workflow: Options-first → Build → Review

For any asset built from a brief, run these three phases in order. Both choosing and reviewing happen through the chat's click interface (AskUserQuestion), which returns Alon's input automatically; the published pages are the visual reference. Never ask for copy-paste or file upload. Surface the URL on every publish.

1. **Options first (see, then choose).** From the brief, build a visual **options page** in the asset's own design language: 2-4 options per section, grouped by angle, the recommendation marked. Publish and send the URL. Then, section by section via the click interface, Alon picks his preferred option (offer a second pick to capture priority order).
2. **Build.** Assemble Alon's chosen options into the clean production asset. Publish and send the URL.
3. **Review together.** Fold by fold, run the tag review (see "Review mode" and "Feedback rubric") on the assembled asset until every message is "loved." Fold each reaction into the skill as you go.

Alon wants to **see options in context before reacting** — leading with a bare list of lines in chat is the wrong default.

## Proposing copy: always give options

**Never return a single message.** Any time you propose copy — a headline, subject line, CTA, tagline, hero line, session title, or any line Alon might use — give **at least 3 options (3-6), grouped by angle**, then recommend one with a one-line rationale tied to the surrounding content. One option is never an acceptable answer to a copy request.

When you present multiple options, add a compact one-line **feedback legend** beneath them so Alon can react in a word (see "Feedback rubric" below). Show the legend only when there is more than one option; skip it for a single locked line.

Typical angles:
- **Pain-point angle.** Names the specific friction. "Your marketing team is still waiting on dev."
- **Direct / value angle.** States the outcome plainly, no metaphor.
- **Win-back / return angle.** Implies something changed since they left, no guilt-tripping.
- **Bold / declarative angle.** Short, confident, often a fragment.
- **`What if...?` angle.** Invites the reader to imagine.

After Alon reacts (rejects, tweaks, or picks a direction), **narrow to refined variants that fold in his specific edit.** Don't restart from scratch. If he flags a typo or asks for an element ("needs a call to Build"), fold it into every subsequent option, not just the one he pointed at.

### Worked example (win-back subject line)
- Draft: "Did you look for a tool for you marketing team?" (typo, generic)
- Refined direction: "Still waiting on dev to build what your marketing team needs?" Ties directly to the dev-bottleneck pain in the body and sets up the "build it yourself" punchline.

## Feedback rubric

Alon's copy feedback clusters into a small, fixed set of tags. Each maps to the rule it signals and to a fixed fix. When he replies with a tag (English or Hebrew) plus which option, act on it directly and narrow on the same direction. Do not restart from scratch.

| Tag (EN / HE) | What it signals | What to do |
|---|---|---|
| loved / אהבתי | It passes | Lock it; save it under `examples/` as an approved line |
| unclear / לא ברור | Too clever or cute in a way that obscures the point: a pun or wink you have to decode (e.g. "The guardians of the galaxAI") | Cut the cleverness; say the one plain thing directly |
| fluff / פלאף | Breaks "no fluff, be specific" | Cut it; replace with something concrete and specific |
| no Value/Outcome / אין Value | Breaks "land on the outcome" | Re-anchor the line to the business or human payoff |
| tactical / טקטי | Breaks the altitude rule | Raise altitude; strip PoC/rollout/ops vocabulary, use strategic framing |
| overlap / חזרתי | Repeats or overlaps another headline (breaks "each section says one new thing") | Re-angle to a distinct facet, or cut; check it against sibling sections, especially the agent-showcase |

Present these as a compact legend under any multi-option set, for example:
> React in a word: loved / unclear / fluff / no-Value / tactical / overlap (+ which option).

**Recurring tags feed the skill.** If the same tag keeps coming up across proposals or sessions, that is a signal the underlying rule needs sharpening. Update the relevant reference file (add a rule, tighten wording, or add an approved / counter example) and commit, per the self-improvement loop.

## Review mode: collect feedback by click, not copy-paste

Before an asset goes to production, collect Alon's per-message feedback through the chat's native question UI (AskUserQuestion), not a copy-paste board or a file upload. He clicks a tag per message and the answers return to you automatically. Present messages in batches (up to 4 per call); each message is one question with the rubric tags as options. The UI caps at 4 options, so show the most relevant tags for that batch and rely on "Other" for the remaining tags and free text. Keep **"unclear" in the default chip set** (Alon values it). A workable default four is Loved / Unclear / Tactical / Fluff-or-no-value, swapping Overlap in when sibling-headline repetition is the live risk. Then learn from each reaction (sharpen the skill), and present alternatives for the flagged ones the same way, until each message is "loved." A published artifact can show the messages in context, but the reactions come through the question UI. Never ask Alon to copy-paste or upload his feedback.

## Iterate line-by-line

- When Alon approves a section, **freeze it** and move to the next. Don't regenerate whole blocks.
- When he gives a one-line correction ("'our product marketing team,' not 'our team'," or "just remove 'the'"), apply it **exactly at that spot, precisely and minimally.** Don't touch surrounding text he didn't flag.
- **When he rejects everything with no reason** ("לא אוהב אף אחד מהם" / "don't like any of these"), don't guess and burn another round in the same failed direction. Ask what's off first: too dramatic? too generic? not connected to the content?
- Do real analysis before recommending. If asked to pick between options (copy, naming, ordering), check how each connects to the specific content already in the asset, not a surface gut read. Don't undersell an option first and discover its justification only when pushed.

## Don't present unverifiable specifics as fact

This skill does not carry monday's live inventory of agents, apps, integrations, or customers. So when an asset needs concrete specifics you cannot verify (named example agents, products, integrations, customer names, stats), treat them as **illustrative recommendations to validate**, never as an existing catalog. Flag it visibly on the asset itself (a short note placed as a side annotation, not a subheadline) and call it out in the handoff. Example note: "Recommended examples, not existing agents. Validate each against monday's current agent catalog before use." Prefer real, public claims (250,000+ customers, Gartner Leader) over invented specifics.

## Delivery: one shareable link per asset

Every finished asset ships as its **own published artifact with its own shareable URL**, so Alon can share each one independently. One asset per link. Never combine assets into one artifact. Render each in the form that fits it:
- **Landing page** -> a rendered HTML page.
- **Email** -> a rendered HTML email (email width, realistic layout).
- **Session titles / naming** -> a clean rendered page listing them.
- **Presentation / deck** -> a rendered HTML slide deck (offer a `.pptx` export as a separate file when an editable deck is needed).

Keep review/comparison boards (options per fold) as their own separate artifact, distinct from the final asset. Artifacts start private; Alon shares them from the page's share menu. Render monday-branded drafts with a visible "draft" marker and placeholder proof (no fabricated customer records).

**Always surface the artifact's URL as plain, visible text in the reply** every time you publish or update an asset, not only as a linked word. Alon wants the raw URL each time.

## Language default

Output English for anything customer-facing or product copy, even though Alon writes to Claude in Hebrew. Keep the conversation in Hebrew; keep the deliverable in English unless told otherwise.

## First-person / narrative voice (Customer Zero, LinkedIn, interview prep)

The discipline stays; the voice warms.
- **Concrete sensory detail over abstraction.** "Walking the hallways with my laptop" beats "I was excited."
- **Names and titles exact.** Verify roles (e.g. get CEO vs. CTO right). Getting a name wrong breaks trust instantly.
- **Close to the reader, don't summarize.** The last line speaks directly to the viewer.
- **No motivational-quote or fake-dialogue openers.** Prefer a real question or a concrete moment.

## Design-system restraint (when copy goes into HTML/decks/emails)

Alon cares about visual restraint as much as copy restraint:
- No gradients.
- One accent color, used consistently and meaningfully, not decoratively.
- A technical/monospace font paired with a humanist sans.
- Consistent divider and section patterns.

If it's unclear which system applies (Readout deck vs. dark vision-page vs. email), **ask which artifact this is for before assuming.**

## Commit / version discipline (for repo work)

Ship small, descriptive commits, one change per commit (matches how the deck repo is maintained). Commit and push exploratory/review variants too, not just finals. Everything version-controlled.
