# Layout & Components

## Layout grid and rhythm

- **Container:** center content in a `max-width` around 1080-1180px with `padding: 0 24px`. Wide content (tables, code, diagrams) scrolls inside its own `overflow-x: auto` box so the page body never scrolls sideways.
- **Section rhythm:** lay out sibling groups with flex/grid and `gap`, not per-element margins. Sections get generous vertical padding (~60-74px) and a `1px solid var(--line)` top border for a steady beat. First section has no top border.
- **Split rows:** a common section is a two-column split (headline left, supporting lead right) that stacks on mobile.
- **Cards:** `background: var(--panel)`, `1px solid var(--line)`, radius ~14px, generous inner padding. Moderate radii, not `rounded-lg` on everything.
- **Spec-sheet pattern:** for pillars/attributes (Transparency / Accountability / Control / Security), a bordered "sheet" with rows separated by hairlines, each row a mono label + a one-line value. Reads as a considered spec, not decoration.
- **Allocation / org map:** to present a structure to a stakeholder (team split, org shape, funnel routing), make the *layout itself* carry the argument — a dark root node with a headcount pill, a short stem, then N sibling columns for the groups. Each column leads with the number set big in the accent (`2` / `3` / `1`), a mono group label, a one-line role, and a footer detail (segment chips, product list, or model). The relative weights read at a glance before anyone parses a word. Prefer this over a dense matrix/table when the goal is for someone to *see* the model, not decode it; reserve the table for when exact per-cell precision is the point.
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
