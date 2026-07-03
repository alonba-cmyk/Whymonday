# Build Brief — mondaystorydeck-shortpitch.html

## The Task

Duplicate `mondaystorydeck-agents.html` into a new file `mondaystorydeck-shortpitch.html`.  
This is a shorter, more narrative sales pitch — same visual language and tech stack, different story.  
~80% of the existing file transfers unchanged.

**Work needed:**
- Remove 4 slides
- Edit text in 2 slides
- Add 2 new slides
- Update the JS slide order array

---

## Repo & Setup

| | |
|---|---|
| Repo | alonba-cmyk/Whymonday |
| Branch | `claude/monday-story-deck-v6idf5` |
| Base file | `mondaystorydeck-agents.html` |
| Output file | `mondaystorydeck-shortpitch.html` |

---

## Story Outline — 10 Beats

### Act 1 — Vision
**Beat 1 — Hero opening**  
"People and agents. Working together." — פותחים בחזון, לא בבעיה.  
→ S0, no changes

### Act 2 — Problem
**Beat 2 — "Running at 100%"**  
"Your team is already running at 100%. More requests. More priorities. Same hours."  
הבעיה היא capacity, לא יכולת.  
→ NEW SLIDE — insert after S0

**Beat 3 — Why agents aren't helping**  
No shared workspace. No one managing them. No context. Siloed output.  
→ S3b — text change in 2 of 4 cards

### Act 3 — Solution
**Beat 4 — Agents as teammates**  
"What if agents weren't tools you prompt — but teammates who join your team?"  
They take on tasks. They work in context. They scale your capacity.  
→ S2 — headline + subtext change only

**Beat 5 — monday built for this**  
"One place where people and agents plan, execute, and deliver — together."  
→ S5, no changes

**Beat 6 — Workspace · Context · Control**  
Three pillars — where agents work, what they know, who manages them.  
→ S5 layers, no changes

**Beat 7 — Build by describing it**  
"Create apps, automate workflows, deploy agents — just tell monday what you need."  
→ NEW SLIDE — insert before S6

### Act 4 — Proof & Close
**Beat 8 — Social proof** → S5b, no changes  
**Beat 9 — Monday on Monday** → smom, no changes  
**Beat 10 — CTA** → S6, no changes

---

## Slide-by-Slide Plan

### S0 — Hero ✓ Direct
No changes. Mobile hero animation included.

---

### NEW — "Running at 100%" (insert after S0)
Style: same as S3b (cards on dark background).

**Headline:** "Your team is already running at 100%."  
**Sub:** "More requests. More priorities. Same hours."  
**3 pain-point cards:**
- "Requests pile up"
- "Priorities conflict"
- "There's never enough time"

---

### S2 — What's changed → Teammates (~Text change)
Keep all visuals (AI logos marquee, layout). Change headline + subtext only.

**Before:** "Now, work can get done faster with agents doing the work for you"  
**After:**  
Headline: "Meet your new teammates."  
Sub: "Agents aren't tools you prompt — they join your team, take on tasks, and scale your capacity."

---

### S3b — Why agents aren't making a difference (~Text change)
Keep layout (4 cards). Replace 2 cards, keep 2.

**Replace:**
- ❌ "Individual AI" → ✓ "No shared workspace"
- ❌ "Lack of adoption" → ✓ "No one managing them"

**Keep unchanged:**
- ✓ "Lack of context"
- ✓ "Siloed Output"

---

### S5 — AI Work Platform ✓ Direct
No changes.

### S5 Layers — Workspace / Context / Control ✓ Direct
No changes.

---

### NEW — "Build by describing it" (insert after S5 Layers, before S5b)
Style: match existing slides. Light visual: prompt input → result appears.

**Headline:** "Build it by describing it."  
**Sub:** "Create apps, automate workflows, and deploy agents — just by telling monday what you need."  
**Visual:** Simple prompt → output animation (text typed in → result card appears)

---

### S5b — Social Proof ✓ Keep (present in both decks)
### smom — Monday on Monday ✓ Keep (present in both decks)
### S6 — CTA ✓ Direct — no changes

---

### Slides to REMOVE entirely
- S1 — Mission carousel
- S3 — 95% gap stat (MIT Sloan)
- sstory — Customer story
- scred — Credentials

---

## Final Slide Order

S0 → **NEW: Running at 100%** → S2 (updated) → S3b (updated) → S5 → S5 Layers → **NEW: Build by describing** → S5b → smom → S6

---

## Technical Notes

### File structure
Each slide is a `<section id="sX">` element. Navigation is driven by a JS array — update it to match the new slide order after adding/removing sections.

### JS hooks
```js
// Runs each time a slide becomes active:
onSlideEnter(n) { ... }

// Mobile hero replay (S0 only):
function s0MobPlay() { ... }
// Called inside onSlideEnter when n === 0 && window.innerWidth <= 768

// Force CSS transition restart trick:
void el.offsetWidth;
```

### Mobile hero (S0)
The mobile hero is inside `#s0` as `.s0-mob-hero`. Hidden on desktop via `@media (min-width: 769px)`. The desktop version is hidden on mobile via `@media (max-width: 768px) { #s0 .s0-body { display:none } }`. Do NOT move this to an unconditional rule — cascade order matters.

### Design tokens
```
--purple: #6161ff
--bg:     #000
Font:     Poppins (loaded via Google Fonts link in <head>)
Images:   https://uauxewnxnprttvxnvsit.supabase.co/storage/v1/object/public/
```

### New slides — match S3b style
Both new slides should visually match S3b: cards on dark background, same font sizing, same border treatment. Copy the S3b section as a starting point and adapt the content.
