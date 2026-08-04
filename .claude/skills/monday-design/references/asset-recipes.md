# Asset Recipes

Per-artifact design. Each reuses the foundations, layout, and components; the recipe is the arrangement.

## Landing page

- **Header:** static top bar with the tri-dot mark + `monday.com` wordmark, light nav, a theme toggle, and (on drafts) a review bar above it.
- **Hero:** faint subject-grounded background texture (e.g. a blueprint grid via hairline `repeating-linear-gradient`, kept very subtle — a grid texture, not a color gradient). Big broken-line headline, one accent CTA + one ghost CTA, a mono "spec strip" of key facts.
- **Trust bar:** mono "Trusted by 250,000+ teams" + a row of neutral placeholder logo pills.
- **Body sections** on the section-rhythm grid: division-of-labor split, agent showcase (ID cards), a shared-workspace section (a centered headline + a "feed" panel of person/agent rows + a grid of value boxes with a short accent bar each), a "build tools" section, proof (`Recognized by analysts, loved by users` + badges), and enterprise-trust as a spec sheet.
- **Close:** centered CTA echoing the throughline.
- Footer: mono divider note + a "draft" line on drafts.

## Marketing email

- Render as a **real email preview**: a centered card (~600px) on a neutral backdrop, not a full-bleed page.
- Above the card, show the **subject line and preview text** as labeled meta (mono `Subject` / preview snippet) so both are reviewable.
- Card: a slim header with the wordmark, a body with a bold headline (line-break rule applies), one or two short paragraphs, an accent CTA button, and a muted compliance footer.
- Keep it tight: two sentences per paragraph, one accent action.
- Drafts get the review bar + theme toggle around the preview; the card itself stays clean.

## Pitch / story deck

- Slide-shaped sections in the same token system. Eyebrow (category, mono) → headline (one claim, broken-line) → subhead → supporting visual or bullets.
- Consistent per-slide structure; the eyebrow never repeats the headline. Strong type, lots of air, one accent.
- Dark theme reads well for a keynote feel, but still default light with the toggle.

## Options / review board

- A vertical list of **folds/elements**, each a numbered section (mono number chip) with a short note and a grid of option cards.
- Each option card: a mono angle tag, the option text, a letter, and a `Rec` chip on the recommendation (accent-outlined card).
- Top: a sticky review context bar + theme toggle. This is a working surface, so density over decoration; the copy is the content.

## Session-title / naming page

- A clean program layout: each session is a row with the audience + its "wants" on the left (mono + bold) and the `hook : descriptor` on the right, the hook bold, the colon in the accent, the descriptor muted below. Hairline dividers between rows.

## Diagrams

When a diagram genuinely helps (a flow, an architecture, a timeline), draw the real mechanism with inline SVG that reads in both themes (stroke via `currentColor` / tokens). Load the `artifact-diagramming` skill for the mechanics. Don't decorate with a diagram that carries no information.
