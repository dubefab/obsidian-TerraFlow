# TerraFlow

A seasonal Obsidian theme with 11 palettes, deep [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) integration, and a Minimal/Baseline/Cupertino-compatible cssclass vocabulary. Works with or without the Style Settings plugin — every feature has a sane fallback.

## Seasons

Pick one from Style Settings → TerraFlow → Color Scheme → Active Season. Each ships light and dark variants except Academia, which is dark-only.

<p>
  <img src="screenshots/autumn-dark.png" width="32%" alt="Autumn, dark">
  <img src="screenshots/autumn-light.png" width="32%" alt="Autumn, light">
  <img src="screenshots/tokyo-night-dark.png" width="32%" alt="Tokyo Night, dark">
</p>
<p>
  <img src="screenshots/iceberg-light.png" width="32%" alt="Iceberg, light">
  <img src="screenshots/melange-light.png" width="32%" alt="Melange, light">
</p>

*Four of the eleven seasons shown above (Autumn in both modes, plus Tokyo Night, Iceberg, and Melange). The remaining seven — Spring, Summer, Winter, Academia, Twilight, Paper, Calm Focus — follow the same design; switch Active Season in Style Settings to preview any of them live in your own vault.*

| Season | Feel |
|---|---|
| 🌱 Spring | Fresh greens, soft pastels |
| ☀️ Summer | Bright, warm, high-energy |
| 🍂 Autumn | Warm clay and amber (default) |
| ❄️ Winter | Cool blues, crisp contrast |
| 🧊 Iceberg | Arctic blue-gray, low saturation |
| 📚 Academia | Dark oak and ink, library-quiet |
| 🌙 Twilight | Deep purple-blue dusk |
| 📄 Paper | Sepia, reads like a printed page |
| 🍃 Calm Focus | Low-chroma sage-clay, Braun/Muji-quiet |
| 🏜️ Melange | Desert neutrals |
| 🌆 Tokyo Night | Neon-on-navy |

A Custom Accent Color toggle overrides any season's accent with your own color, and P3 Vivid Accents chroma-boosts the accent on wide-gamut displays.

## Coming from Minimal, Baseline, or Cupertino

TerraFlow speaks the same cssclass vocabulary those themes use, so notes written for them render correctly here without edits:

- Block width: `wide` / `max` / `table-wide` / `table-100` / `table-max` / `img-wide` / `img-100` / `img-max` (TerraFlow's own `wide-page` / `full-page` / `wide-table` / `wide-image` still work — both names are accepted)
- Image filters: `#invert`, `#invertW`, `#circle`, `#outline`, `#blend`, `#interface` — append to the image path (`![[photo.jpg#invert]]`)
- `img-grid` — consecutive images flow side by side instead of stacking (reading mode)
- `embed-strict`, `embed-hide-title` — strip an embedded note's card chrome or title bar
- Table helpers — see below
- Card and banner classes — see below
- ~30 alternate checkbox states — see below

## Style Settings reference

Style Settings → TerraFlow groups everything under these headings:

**Color Scheme** — season, custom accent, monochrome mode, low contrast mode, heading color intensity, season-tinted body text, P3 vivid accents, custom per-level heading colors (H1–H6).

**Interface** — interface layout, depth & shadows (plus tinted ambient shadows / luminance-depth alternatives), Quiet Mode (Rams reduction), neutral chrome, file explorer style, floating nav buttons, hover-to-show view header, auto-hide ribbon, ambient accent gradient, scroll edge dissolve, soft pill tabs.

**Liquid Glass** — glass tint strength, and per-surface toggles for tags, the properties panel, tables, the status bar, and the command palette.

**Animations** — animation style (off / default / whimsy), smooth iA Writer-style caret, reading progress bar, scroll-reveal.

**Editor & Content** — body text weight, optical text centering, balanced headings, luminous details (glowing hairlines + image hover lift), elegant embed cards, aurora note title, link style, highlight style, blockquote style, callout style, accent inline code, tabular numerics, Braun tag chips, fancy multilevel bullets, accent caret & selection, static caret, **season-colored diagrams** (Mermaid — see below).

**Headings** — heading style, alignment, font, tight tracking, per-level case (title/sentence/upper/lower) for H1–H6.

**Alternate Checkboxes**, **Tables** (density, striping, hover), **Layout & Spacing** (line width, line height, focus dot grid), **Block Width** and **Banners & Cards** cssclass reference panels, **Deep Focus Mode** (typewriter dimming, hide sidebars, keep chrome), **Performance & Accessibility** (kill switches for UI animations, modal frost, glass menus, box shadows, scrollbar styling, status bar styling).

## Graph view and canvas

Graph view, canvas, and any plugin reading Obsidian's base `--color-red/green/yellow/.../--color-base-00…100` ramp now render in the active season instead of Obsidian's stock hues — this ramp is derived from each season's own callout colors, so it updates automatically when you switch seasons.

## Mermaid diagrams

Diagrams color from the active season instead of Obsidian's default (a raw `invert()` filter that mangles hue in a warm palette). Toggle **Season-Colored Diagrams** off to fall back to Obsidian's native handling.

## Cssclass reference

Add any of these to a note's `cssclasses` frontmatter field.

**Width**
`wide-page` / `wide`, `full-page` / `max`, `wide-table` / `table-wide` / `table-100` / `table-max`, `wide-image` / `img-wide` / `img-100` / `img-max`

**Tables**
`table-nowrap`, `table-wrap`, `table-center`, `table-numbers`, `table-small`, `table-tiny`, `table-lines`, `row-lines`, `col-lines`, `row-alt`, `col-alt`

**Cards** (renders a Dataview table as a card grid)
`cards`, `cards-cols-1` … `cards-cols-8`, `cards-16-9`, `cards-1-1`, `cards-2-1`, `cards-2-3`, `cards-cover`, `cards-align-bottom` — set `--cards-min-width` via Style Settings for the auto-fit default. Column and aspect-ratio classes are Dataview-only; Bases' native card view positions cards with JS, not CSS grid, so it can't take a column count.

**Banners** (`![[image.jpg|banner]]`)
`banner`, `banner-fade`, `banner-icon` (tag a second image `![[icon.png|banner-icon]]`), `banner-title`, `y0` … `y100` in steps of 5 (vertical crop position)

**Embeds**
`embed-strict`, `embed-hide-title`

**Images**
`img-grid` · filters via path suffix: `#invert`, `#invertW`, `#circle`, `#outline`, `#blend`, `#interface`

## Checkboxes

Enable **Alternate Checkboxes** in Style Settings, then use any of these task markers:

`[/]` in progress · `[-]` cancelled · `[>]` forwarded · `[<]` scheduled · `[?]` question · `[!]` important · `[*]` star · `["]` quote · `[b]` bookmark · `[i]` information · `[I]` idea · `[p]` pro · `[c]` con · `[u]` up · `[d]` down · `[S]` savings · `[k]` key · `[f]` fire · `[t]` time · `[n]` note · `[l]` location · `[w]` win · `[B]` brainstorm · `[L]` love · `[+]` add · `[A]` alarm · `[R]` review · `[P]` phone

Colors ride the season palette, so every season recolors them automatically.

## Print / PDF export

Notes export to a flat, ink-safe light page regardless of the active season or mode — dark backgrounds, glows, and shadows don't survive on paper, so print output deliberately ignores the screen palette. Callouts and code blocks keep a plain border for structure; the on-screen line-width cap is lifted to use the full page width.

## Credits

Card and table treatments adapted from [Baseline](https://github.com/aaaaalexis/obsidian-baseline) (MIT) and the Cards snippet by [@kepano](https://github.com/kepano) (MIT). Checkbox state set inspired by Baseline. Block-width cssclass mechanism inspired by Baseline.

## License

MIT — see [LICENSE](LICENSE).
