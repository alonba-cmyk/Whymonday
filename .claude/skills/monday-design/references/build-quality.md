# Build Quality

How the page is actually built, so it renders cleanly, everywhere, in both themes.

## Self-contained (strict CSP)

Published artifacts run under a strict CSP that blocks every external request.
- **No external fonts, stylesheets, scripts, images, or fetches.** Inline all CSS and JS. Use system font stacks (no webfont URLs). Embed any real asset as a `data:` URI.
- Native mermaid is available via ```mermaid fences / `<pre class="mermaid">` if a diagram needs it; otherwise inline SVG.
- Keep the rendered page under 16MB (data URIs count).

## Responsive

- Relative units, flex/grid with `gap`, `max-width: 100%` on media.
- The page body never scrolls horizontally; wide content (tables, code, diagrams) gets its own `overflow-x: auto` container.
- Grids collapse gracefully (3 → 2 → 1 columns); hide or restack decorative floats on small screens.

## Theme correctness

- Both themes fully styled through tokens; defaults to light (force at top).
- The accent stays legible on both grounds; if it fights the ground, shift it toward analogous or drop saturation rather than swapping hue.
- Test the light/dark toggle and the viewer's own toggle both flip cleanly.

## Accessibility & polish

- Visible keyboard focus states. Sufficient contrast in both themes.
- Respect `prefers-reduced-motion`.
- Close every non-void tag, double-quote attributes.
- `text-wrap: balance` on headings; `tabular-nums` on aligned digits.

## Cascade hygiene

- Watch selector specificity — don't let a type selector fight an element selector over spacing. Structure the cascade so it doesn't silently undo your layout.
- Lay out spacing with `gap`, not margins that collapse or double.

## Artifact metadata

- Set a stable `<title>`, a one-line `description`, and an emoji `favicon`. Keep the favicon stable across redeploys of the same artifact; only change it on a hard topic pivot.
- Redeploy to the same file path to keep the same URL. Always surface the URL as plain text in the reply.

## Pre-publish checklist

1. Defaults to light, both themes styled, toggle works?
2. One accent, no gradients, neutrals hue-biased?
3. Sans + mono pairing; mono on eyebrows/labels?
4. Headline line-break rule applied where a period splits a headline?
5. Self-contained — no external requests, everything inlined?
6. Responsive, no horizontal page scroll?
7. Draft chrome present on drafts / stripped on production?
8. Placeholder logos + real public proof only, no fabricated records; validate-notes out of the reading flow?
9. Focus states, reduced-motion, clean markup?
10. Stable title, description, emoji favicon; URL surfaced in the reply?
