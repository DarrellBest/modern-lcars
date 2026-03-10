# Modern LCARS

A modern take on the LCARS (Library Computer Access/Retrieval System) design language — inspired by the newer Star Trek series (Discovery, Picard, Strange New Worlds). Glass morphism, fluid animations, holographic effects, and refined geometry.

## Philosophy

Classic LCARS (TNG era) was bold, blocky, and vivid. Modern LCARS evolves this with:

- **Glass morphism** — frosted translucent panels with backdrop blur
- **Refined palette** — warm ambers and golds paired with cool ices and violets
- **Fluid motion** — spring-based easing, staggered entrances, ambient scanners
- **Thinner geometry** — lighter borders, subtler elbows, breathing room
- **Holographic touches** — shimmer effects, pulse glows, conic gradient overlays

## Quick Start

```html
<link rel="stylesheet" href="src/css/modern-lcars.css">
```

Or serve locally:

```bash
npx serve . -p 8600
```

Then open any example:
- `/examples/dashboard/` — Full operations dashboard
- `/examples/controls/` — Component showcase (colors, typography, buttons, forms, animations)
- `/examples/starship-monitor/` — Interactive starship systems monitor with live data

## Design Tokens

All customizable via CSS custom properties (`--ml-*`). See `src/css/tokens.css` for the full list.

### Core Colors
| Token | Color | Use |
|-------|-------|-----|
| `--ml-amber` | #F4A261 | Primary accent, engineering |
| `--ml-gold` | #E9C46A | Values, warnings |
| `--ml-ice` | #76C7F0 | Tactical, secondary |
| `--ml-cyan` | #56E3E3 | Operations, info |
| `--ml-violet` | #9B72CF | Science, accent |
| `--ml-mint` | #80FFDB | Success, medical |
| `--ml-coral` | #FF6B6B | Danger, alerts |

### Typography
- **Display**: Chakra Petch (headers, titles)
- **Body**: Inter (readable body text)
- **Mono**: JetBrains Mono (data, labels, code)

## Components

| Component | Class | Description |
|-----------|-------|-------------|
| Panel | `.ml-panel` | Glass-morphism card with optional `data-accent` |
| Header | `.ml-header` | Signature pill + bar navigation header |
| Sidebar | `.ml-sidebar` | Vertical colored block navigation |
| Button | `.ml-btn` | Pill-shaped action buttons |
| Input | `.ml-input` | Styled text/select/textarea |
| Range | `.ml-range` | Styled range slider |
| Stat | `.ml-stat` | Label/value data row |
| Table | `.ml-table` | Styled data table |
| Badge | `.ml-badge` | Inline status indicator |
| Tag | `.ml-tag` | Subtle metadata label |
| Progress | `.ml-progress` | Gradient progress bar |
| Alert | `.ml-alert` | Notification banner |
| Divider | `.ml-divider` | Gradient horizontal rule |
| Elbow | `.ml-elbow` | Classic LCARS elbow shape (modernized) |

## Animations

| Class | Effect |
|-------|--------|
| `.ml-animate-fade` | Fade in |
| `.ml-animate-up` | Slide up + fade |
| `.ml-animate-right` | Slide right + fade |
| `.ml-animate-scale` | Scale in |
| `.ml-animate-pulse` | Ambient glow pulse |
| `.ml-animate-blink` | Blinking indicator |
| `.ml-holo` | Holographic shimmer overlay |
| `.ml-scanner` | Scanning line effect |
| `.ml-stagger` | Staggered children entrance |

## Layout

| Class | Description |
|-------|-------------|
| `.ml-app` | Flex app shell |
| `.ml-grid` | CSS grid container |
| `.ml-grid--2/3/4` | Column variants |
| `.ml-grid--auto` | Auto-fit responsive grid |
| `.ml-flex` | Flex utilities |

## Assets

SVG building blocks in `src/assets/`:
- `elbow-top-left.svg` — Top-left elbow connector
- `elbow-bottom-left.svg` — Bottom-left elbow connector
- `pill.svg` — Rounded pill shape

## License

MIT
