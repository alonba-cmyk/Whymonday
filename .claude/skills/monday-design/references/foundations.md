# Foundations: Brand, Color, Typography, Theme

## Brand identity

monday.com's surfaces read **friendly and bold**: confident heavy headlines, rounded corners, generous whitespace, playful energy, and the tri-color mark (a pink/red capsule, a yellow capsule, a green dot). Marketing pages use 3D character avatars and colorful product UI (status pills, boards).

Alon's build keeps the friendly-bold foundation but **disciplines it into something cleaner and more editorial**: one accent instead of the full rainbow, a mono for labels, and real restraint. The result should feel unmistakably monday, but composed, not busy.

- **The mark:** a small three-dot lockup (pink/red, yellow, green) next to the `monday.com` wordmark in the header. Use it as a light brand cue, not a hero element.
- **Placeholders, never fakes:** stock-style photos and named customer quotes are replaced with neutral placeholder logos/avatars and real public proof (250,000+ customers, Gartner Leader). Never fabricate a customer record.

## Color

**One accent, grounded in the subject.** Pick a single accent color that belongs to the asset's world, and use it only for emphasis, links, and the primary action. No gradients anywhere.
- Construction → a marigold "site-marker" amber on cool blueprint-navy neutrals.
- GTM / event / email → a confident violet/indigo.

**Neutrals are chosen, not defaulted.** Bias the greys slightly toward the accent's hue (a cool blueprint-navy grey, a violet-tinted grey), never pure `#808080`. Grounds are near-white in light and a deep tinted near-black in dark.

**Semantic color is separate from the accent.** Good/warning/critical (a green, an amber, a red) are their own signals and never count as the accent.

Define the whole palette as CSS custom properties (tokens), then style everything through the tokens. Typical token set:
`--ground, --panel, --panel-2, --ink, --ink-soft, --ink-faint, --line, --accent, --accent-ink, --accent-tint`.

## Typography

**Pair a humanist sans with a mono.** No webfonts — the Artifact CSP blocks font CDNs and a linked webfont fails silently. Use strong system stacks:
- Sans (headings + body): `"Segoe UI", system-ui, -apple-system, Roboto, Helvetica, Arial, sans-serif`.
- Mono (eyebrows, labels, spec annotations, data): `ui-monospace, "SF Mono", "JetBrains Mono", Menlo, Consolas, monospace`.

The **mono is the signature move** — use it for uppercase eyebrows, small category tags, spec-sheet labels, and dimension-style annotations. It gives the technical-but-warm, blueprint-annotation feel.

- **Headlines:** heavy weight (800), tight letter-spacing (about `-0.02em`), `text-wrap: balance`, large clamp scale (e.g. `clamp(1.8rem, 3.6vw, 2.5rem)` for h2, larger for hero).
- **The line-break rule:** in a headline, a sentence-ending period followed by more text breaks to a new line via `<br>`, so each sentence is its own line ("You run the build. / Agents run the coordination."). A comma or a final-only period does not break. Use judgment; skip if it orphans an awkward fragment.
- **Body:** ~1.05rem, line-height ~1.6, max width ~62ch.
- **Eyebrows/labels:** mono, ~0.66rem, uppercase, letter-spacing ~0.14em, in the accent or a faint ink. An eyebrow never restates the headline.
- Reach for `font-variant-numeric: tabular-nums` wherever digits align.

## Theme (light-default, both fully designed)

Every page is theme-aware and **defaults to light**, with a light/dark toggle in the header.

**Token pattern (robust in both themes and against the viewer's toggle):**
1. Define the palette on `:root` (light values).
2. Redefine only the tokens under `@media (prefers-color-scheme: dark)`.
3. Redefine them again under `:root[data-theme="dark"]` and `:root[data-theme="light"]` so the in-page toggle and the viewer's toggle both win.
4. Style components only through the tokens, never inside the media query.

**Force the light default** at the very top of the page so it opens light regardless of the viewer's system theme:
```html
<script>document.documentElement.setAttribute('data-theme','light');</script>
```

**Header light/dark toggle** (icon swaps sun/moon by current theme):
```html
<button id="themeBtn" class="theme-toggle" aria-label="Toggle light or dark mode"><span class="ti"></span></button>
```
```js
var root = document.documentElement, tb = document.getElementById('themeBtn');
var SUN = '<svg ...sun...>', MOON = '<svg ...moon...>';
function current(){ return root.getAttribute('data-theme') ||
  (matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light'); }
function render(){ tb.querySelector('.ti').innerHTML = current()==='dark' ? SUN : MOON; }
tb.addEventListener('click', function(){ root.setAttribute('data-theme', current()==='dark'?'light':'dark'); render(); });
render();
```
Give dark the same care as light: don't invert naively; keep contrast legible and the accent working on both grounds.
