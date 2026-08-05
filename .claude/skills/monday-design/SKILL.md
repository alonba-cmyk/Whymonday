---
name: monday-design
description: Alon's (VP Product Marketing, monday.com) visual design system for customer-facing and GTM assets — landing pages, marketing emails, pitch/story decks, options/review boards, session-title pages, and any rendered HTML artifact for monday.com. Use whenever you're designing or building the look of a monday asset: choosing palette, typography, layout, components, or theming. Trigger even if Alon doesn't say "design" — any request to build, render, restyle, or lay out a monday page or deck should default to this system. Pairs with the monday-messaging-voice skill (that one owns the words; this one owns the look).
---

# monday Design System (Alon's build)

The visual counterpart to `monday-messaging-voice`. That skill owns the words; this one owns the look. Distilled from monday.com's own marketing surfaces (persona landing pages, product pages, Vibe emails, in-product modals) and from the design decisions Alon approved while building assets: a clean, editorial, restrained take on monday's friendly-bold brand.

Like the voice skill, this is **living** — fold Alon's design feedback into these files and commit, so it sharpens every session.

## The design in one breath

monday's friendly-bold foundation (rounded, generous whitespace, confident type, the tri-color mark), disciplined by Alon's restraint: **one accent used with meaning, no gradients, a humanist sans paired with a mono for labels, consistent structure, and full light/dark that defaults to light.** Ground the accent and any motif in the asset's own subject, so each page looks made for its topic, not templated.

## Non-negotiable rules

1. **Default to light.** Every rendered page opens in light and carries a light/dark toggle in the header (`references/foundations.md` § Theme). Both themes fully designed.
2. **One accent, used meaningfully.** A single accent color, grounded in the subject, used for emphasis and action, never decoratively. No gradients.
3. **Pair a humanist sans with a mono.** Sans for headings and body; a monospace for eyebrows, labels, and spec annotations (the "blueprint annotation" feel). No webfonts (CSP blocks them) — use strong system stacks.
4. **Headline line-break rule.** In a headline, a sentence-ending period followed by more text breaks to a new line, so each sentence sits on its own line (`<br>`). Use judgment; a comma or final-only period does not break.
5. **Restraint over flash.** Choose neutrals with a slight hue bias toward the accent, not pure grey. Generous whitespace. Consistent dividers and section rhythm. Precision beats decoration.
6. **Self-contained.** Inline all CSS/JS, embed assets as data URIs, no external fonts/CDN/requests (strict CSP). Responsive, no horizontal page scroll. Emoji favicon.
7. **Drafts carry review chrome; production strips it.** A draft shows the review bar, the "Show alternatives" toggle, and a draft marker. The production export removes all of it (`references/components.md`).
8. **Never fabricate records.** Use placeholder logos/avatars and real public proof only; flag invented specifics as recommendations to validate (this mirrors the voice skill's accuracy rule).
9. **Equal cards in a group.** Cards/tiles sitting together on the same screen are always the same size as each other (equal height), unless a size difference is deliberate. Never let one- vs multi-line content make one card taller — use `align-items: stretch`, a shared `min-height`, and `-webkit-line-clamp` on variable text, and re-verify at mobile widths (`references/layout-and-components.md` § Cards).

## Workflow

1. **Ground it in the subject.** Pin the subject's world (construction → blueprint grid, marigold site-marker; GTM/event → violet). Derive the accent and any motif from it.
2. **Set the tokens first.** Define the color + type + theme token system (`references/foundations.md`) before laying out.
3. **Lay out on the grid,** using the standard section rhythm and components (`references/layout` and `references/components.md`).
4. **Reuse the standard components** (review bar, toggles, cards, notes) rather than reinventing them.
5. **Match the asset recipe** for the specific artifact (`references/asset-recipes.md`).
6. **Run the build-quality check** before publishing (`references/build-quality.md`).

## Reference index

| File | What's in it |
|---|---|
| `references/foundations.md` | Brand identity, color system, typography, and the theme (light-default) token pattern |
| `references/layout-and-components.md` | Layout grid and section rhythm; the standard components (review bar, alternatives toggle, theme toggle, cards, notes, draft vs. production) |
| `references/asset-recipes.md` | Per-asset design: landing page, marketing email, deck, options/review board, session-title page |
| `references/build-quality.md` | Self-contained/CSP rules, responsiveness, accessibility, and the pre-publish checklist |

Always pair with `monday-messaging-voice` for the copy.
