# Layout & Components

## Layout grid and rhythm

- **Container:** center content in a `max-width` around 1080-1180px with `padding: 0 24px`. Wide content (tables, code, diagrams) scrolls inside its own `overflow-x: auto` box so the page body never scrolls sideways.
- **Section rhythm:** lay out sibling groups with flex/grid and `gap`, not per-element margins. Sections get generous vertical padding (~60-74px) and a `1px solid var(--line)` top border for a steady beat. First section has no top border.
- **Split rows:** a common section is a two-column split (headline left, supporting lead right) that stacks on mobile.
- **Cards:** `background: var(--panel)`, `1px solid var(--line)`, radius ~14px, generous inner padding. Moderate radii, not `rounded-lg` on everything.
- **Equal cards in a group (non-negotiable).** Cards or tiles that sit together on the same screen (agent cards, department/use-case tiles, option cards, value boxes) must be the **same size as each other** — uneven heights from a one- vs two- vs three-line body read as broken. Enforce it: put them in a grid/flex with `align-items: stretch` (equal-height columns), or give the repeated card a `min-height` that fits its tallest member, and clamp variable body text with `-webkit-line-clamp` so no card outgrows the rest. Re-check at mobile widths, where narrower cards wrap text to more lines and break the equality that held on desktop. Only make cards different sizes when the difference is deliberate and meaningful (e.g. a featured card), never as a side effect of content length.
- **Peer choices go side by side, not stacked.** When two (or more) options are meant to be *equal* ways forward — a fork like "let an agent build it" vs "set it up yourself" — lay them out **side by side**, not one above the other. Alon flagged a stacked pair because vertical order reads as ranking ("this one's the important one"). Side-by-side columns (grid `1fr 1fr`, `align-items: stretch`, CTA pinned to the bottom with `margin-top:auto` so both cards match) say "these are equal, pick either." Keep them side by side on mobile too if the choice is meant to feel balanced; trim the card copy so two columns fit a phone rather than falling back to a stack. Reserve a visually dominant "primary" treatment (accent fill/border) for when you *intend* to steer — not for a genuine either/or. Signal each option's nature with a neutral cue instead: an icon and a mono eyebrow naming the mode ("Agent-built" / "Guided").
- **Spec-sheet pattern:** for pillars/attributes (Transparency / Accountability / Control / Security), a bordered "sheet" with rows separated by hairlines, each row a mono label + a one-line value. Reads as a considered spec, not decoration.
- Responsive: relative units, flex/grid, `max-width:100%` on media, grids collapse to fewer columns at ~820px and one column at ~560px.

## Standard components

These are reusable across assets. Prefer them over reinventing.

### Review bar (drafts only)
A sticky bar at the very top, above the page header, that frames the page as a draft and hosts review controls. Accent-tinted, unmissable, stays visible on scroll.
- Left: a mono label like `◱ Review draft` with a short instruction.
- Right: the review controls (Show alternatives toggle, and/or theme toggle).
- Make the page header static (not sticky) so the review bar is the only sticky top element.

### "Show alternatives" toggle (drafts only)
A prominent button (in the review bar) that reveals, under each headline, the runner-up option(s). Toggles a class on `<body>`; CSS `.alt { display:none } body.show-alts .alt { display:flex }`.
- Show **only options Alon approved** as runner-ups, never rejected or unvetted ones. A section with a single approved option shows no alternatives.
- The **production export strips** the toggle, the review bar, and all `.alt` blocks.

### Light/dark toggle (every page)
Icon button in the header, swaps sun/moon by current theme. See `foundations.md` § Theme. Present on drafts and production alike; the page still defaults to light.

### Recommendation / validation note
When the asset shows invented specifics to validate (example agents, etc.), place the note **out of the main reading flow** — a quiet footnote under the content, or a side annotation. Never between a headline and the content it introduces, and never styled like a subheadline. Muted (`--ink-faint`), small, with a mono "Note" tag.

### Agent / persona cards
Small "ID cards": a mono role tag, a monogram avatar chip (initials in an accent-tint circle), a bold name, and a one-line outcome. Used for agent showcases and workspace "feeds" (a person-and-agent conversation shown as rows).

## Draft vs. production

- **Draft** (for review): review bar + draft marker, the alternatives toggle, placeholder proof, the validate note. Defaults to light, has the theme toggle.
- **Production** (to ship / share externally): strip the review bar, the alternatives toggle, and the draft marker. Keep the theme toggle and light default. Real proof/logos swapped in where available. Produce it as its own separate artifact with its own URL.

## Motion

Keep it minimal and purposeful (a hover transition, a reveal). Respect `prefers-reduced-motion`. Extra animation reads as AI-generated; restraint reads as considered.
