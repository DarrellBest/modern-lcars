# Modern LCARS

A production-quality design system inspired by the LCARS (Library Computer Access/Retrieval System) interface language — reimagined for the Discovery, Picard, and Starfleet Academy era. Glass morphism, cinematic animations, holographic effects, and refined geometry built entirely in CSS.

> What would LCARS actually look like if redesigned today inside the Star Trek universe — for real use on starships, stations, labs, and personal devices?

---

## Design Philosophy

Classic LCARS (TNG era) was bold, blocky, and vivid. Modern LCARS evolves this into something cinematic, functional, and believable:

- **Glass morphism** — frosted translucent panels with backdrop blur, giving depth to information layers
- **Refined palette** — warm ambers and golds paired with cool ices and violets, with department-coded color assignments
- **Fluid motion** — spring-based easing, staggered entrances, ambient scanners, cinematic page transitions
- **Thinner geometry** — lighter borders, subtler elbows, breathing room between elements
- **Holographic touches** — shimmer effects, pulse glows, conic gradient overlays
- **Information density** — designed for trained personnel reading 50+ data points under pressure
- **Condition awareness** — the entire UI shifts color, intensity, and urgency across Green/Yellow/Red alert states

### Core Principles

1. **Clarity under pressure** — any crew member should read critical status in 0.3 seconds
2. **Hierarchical color** — color is never decorative; it always encodes department, status, or severity
3. **Geometric identity** — pills, elbows, segmented bars, and rounded blocks are the DNA of LCARS
4. **Living interfaces** — constant subtle motion (scanlines, pulses, energy flows) signals an active system
5. **Responsive adaptation** — from bridge viewscreen to PADD to wrist communicator

---

## Quick Start

### Link the CSS directly

```html
<link rel="stylesheet" href="src/css/modern-lcars.css">
```

### Serve locally

```bash
npx serve . -p 8600
```

### Install via npm

```bash
npm install modern-lcars
```

Then import in your CSS or bundler:

```css
@import 'modern-lcars/src/css/modern-lcars.css';
```

---

## Example Screens

| Screen | Path | Description |
|--------|------|-------------|
| **Dashboard** | `/examples/dashboard/` | Full operations dashboard with gauges, stats, and timeline |
| **Controls** | `/examples/controls/` | Component showcase — colors, typography, buttons, forms, animations |
| **Starship Monitor** | `/examples/starship-monitor/` | Interactive ship systems monitor with live data simulation |
| **Bridge Operations** | `/examples/bridge-ops/` | Tactical overview, shields, navigation, crew, and condition switching |
| **Main Engineering** | `/examples/engineering/` | Warp core, EPS power grid, nacelle status, diagnostics, and plasma flow |
| **Sickbay / Medical** | `/examples/sickbay/` | Patient bio-readouts, EKG, treatment log, medication schedule, triage |

All examples include live data simulation with fluctuating values, dynamic timelines, and interactive elements.

---

## Architecture

```
src/css/
├── modern-lcars.css         # Main entry (imports everything)
├── tokens.css               # Design tokens & CSS custom properties
├── base.css                 # Typography, resets, ambient backgrounds
├── layout.css               # Grid, flex, spacing, responsive utilities
├── components.css           # Core UI components
├── advanced-components.css  # Gauges, tactical, timeline, shields, comm
├── starship-components.css  # Warp core, sensors, transporter, medical, crew
├── conditions.css           # Alert state themes (green/yellow/red)
└── animations.css           # Keyframes, transitions, cinematic effects
```

**Zero dependencies.** Pure CSS. No build step required.

---

## Design Tokens

All values are customizable via CSS custom properties (`--ml-*`). Override them on `:root` or any container to theme an entire section.

### Color Palette

| Token | Hex | Role |
|-------|-----|------|
| `--ml-amber` | `#F4A261` | Primary accent, command department |
| `--ml-gold` | `#E9C46A` | Values, warnings, engineering |
| `--ml-tangerine` | `#E76F51` | Security, urgency |
| `--ml-peach` | `#FFBE98` | Communications |
| `--ml-ice` | `#76C7F0` | Tactical, secondary displays |
| `--ml-cyan` | `#56E3E3` | Operations, active data |
| `--ml-teal` | `#2EC4B6` | Supporting cool accent |
| `--ml-sky` | `#4EA8DE` | Navigation |
| `--ml-violet` | `#9B72CF` | Science department |
| `--ml-lavender` | `#C19EE0` | Counselor, soft science |
| `--ml-magenta` | `#D45DBF` | Anomaly, special alerts |
| `--ml-mint` | `#80FFDB` | Success, medical department |
| `--ml-coral` | `#FF6B6B` | Danger, critical alerts |
| `--ml-cream` | `#FAF0E6` | Neutral text highlight |

### Department Color Assignments

```css
--ml-dept-command:     var(--ml-amber);
--ml-dept-tactical:    var(--ml-ice);
--ml-dept-operations:  var(--ml-cyan);
--ml-dept-science:     var(--ml-violet);
--ml-dept-engineering: var(--ml-gold);
--ml-dept-medical:     var(--ml-mint);
--ml-dept-security:    var(--ml-tangerine);
--ml-dept-comms:       var(--ml-peach);
--ml-dept-navigation:  var(--ml-sky);
--ml-dept-counselor:   var(--ml-lavender);
```

### Surface Colors

| Token | Hex | Use |
|-------|-----|-----|
| `--ml-void` | `#020810` | Pure black background |
| `--ml-deep` | `#06101e` | Deep blue-black |
| `--ml-surface` | `#0a1628` | Main panel background |
| `--ml-elevated` | `#0f1d35` | Raised surfaces |
| `--ml-overlay` | `#152542` | Overlaid elements |

### Typography

| Stack | Font | Use |
|-------|------|-----|
| `--ml-font-display` | Chakra Petch | Headers, titles, readouts |
| `--ml-font-body` | Inter | Body text, descriptions |
| `--ml-font-mono` | JetBrains Mono | Data labels, values, code |

**Size scale:** `--ml-text-2xs` (0.6rem) through `--ml-text-5xl` (5.5rem)

### Motion

| Token | Value | Use |
|-------|-------|-----|
| `--ml-ease-out` | `cubic-bezier(0.16, 1, 0.3, 1)` | Standard exit/entrance |
| `--ml-ease-spring` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | Bouncy/playful |
| `--ml-ease-cinematic` | `cubic-bezier(0.22, 0.61, 0.36, 1)` | Dramatic reveals |
| `--ml-ease-snap` | `cubic-bezier(0.5, 0, 0, 1)` | Quick decisive actions |
| `--ml-duration-fast` | `150ms` | Hover states, micro-interactions |
| `--ml-duration-med` | `300ms` | Panel transitions |
| `--ml-duration-slow` | `600ms` | Entrance animations |
| `--ml-duration-cinematic` | `1000ms` | Page transitions, reveals |

### Spacing

`--ml-space-2xs` (2px) → `--ml-space-xs` (4px) → `--ml-space-sm` (8px) → `--ml-space-md` (16px) → `--ml-space-lg` (24px) → `--ml-space-xl` (40px) → `--ml-space-2xl` (64px) → `--ml-space-3xl` (96px)

### LCARS Geometry Constants

```css
--ml-elbow-width:       80px;
--ml-elbow-radius:      24px;
--ml-bar-height:        24px;
--ml-sidebar-width:     80px;
--ml-sidebar-width-wide: 140px;
--ml-header-height:     48px;
--ml-segment-gap:       3px;
```

---

## Component Library

### Core Components

| Component | Class | Description |
|-----------|-------|-------------|
| Panel | `.ml-panel` | Glass-morphism card with optional `data-accent` color bar |
| Header | `.ml-header` | Signature pill + bar navigation header |
| Sidebar | `.ml-sidebar` | Vertical colored block navigation (`.ml-sidebar--wide` for labels) |
| Button | `.ml-btn` | Pill-shaped action buttons (6 colors + ghost + danger + sizes) |
| Input | `.ml-input` | Styled text/select/textarea |
| Search | `.ml-search` | Icon + input search field |
| Range | `.ml-range` | Styled range slider with glowing thumb |
| Stat Row | `.ml-stat` | Label/value data display |
| Table | `.ml-table` | Styled data table with hover states |
| Badge | `.ml-badge` | Inline status indicator (7 variants) |
| Tag | `.ml-tag` | Subtle metadata label |
| Progress | `.ml-progress` | Gradient progress bar (4 color variants) |
| Alert | `.ml-alert` | Notification banner (info/warning/danger/success) |
| Modal | `.ml-modal` | Centered dialog with backdrop blur |
| Toast | `.ml-toast` | Slide-in notification |
| Drawer | `.ml-drawer` | Slide-in detail panel from right edge |
| Spinner | `.ml-spinner` | Loading indicator (3 sizes) |
| Skeleton | `.ml-skeleton` | Content placeholder shimmer (text/title/card/avatar) |
| Accordion | `.ml-accordion` | Expandable content sections |
| Tabs | `.ml-tabs` | Tabbed navigation |
| Breadcrumb | `.ml-breadcrumb` | Path navigation |
| Divider | `.ml-divider` | Gradient rule (or `.ml-divider--lcars` for segmented) |
| Elbow | `.ml-elbow` | Classic LCARS L-shaped connector |
| Log | `.ml-log` | Code/terminal output viewer |
| Empty State | `.ml-empty` | Placeholder for empty data regions |

### Advanced Components

| Component | Class | Description |
|-----------|-------|-------------|
| Gauge | `.ml-gauge` | Radial SVG gauge (sm/md/lg, 5 color variants, auto-threshold) |
| Sparkline | `.ml-spark` | Inline SVG trend chart |
| Timeline | `.ml-timeline` | Event log with colored dot indicators |
| Tactical Radar | `.ml-tactical` | Circular radar with sweep, rings, and contact blips |
| Shield Status | `.ml-shields` | 4-quadrant shield display with health states |
| Section Status | `.ml-section-status` | Deck-by-deck colored segment bar |
| Readout | `.ml-readout` | Large single-value display with glow |
| Comm Channel | `.ml-comm` | Communications panel with channel list and waveform |
| Panel Header | `.ml-panel-header` | LCARS-style colored tab + bar panel title |
| Elbow Frame | `.ml-elbow-frame` | Full corner frame using elbows |
| Stat Card | `.ml-stat-card` | Compact info block with value, label, and trend |

### Starship Components

| Component | Class | Description |
|-----------|-------|-------------|
| Warp Core | `.ml-warp-core` | Animated vertical column with energy rings and plasma glow |
| Power Grid | `.ml-power-grid` | EPS node network with status indicators |
| Power Flow | `.ml-power-flow` | Animated energy flow line |
| Sensor Array | `.ml-sensor-array` | Multi-band sensor bars with color-coded fills |
| Transporter | `.ml-transporter` | Pad array with lock/energize/ready states |
| Crew List | `.ml-crew-list` | Compact crew roster with rank, avatar, and status |
| Diagnostic | `.ml-diagnostic` | System-by-system status checklist |
| Bio-Readout | `.ml-bio-readout` | Patient vitals with EKG line and alerts |
| Frequency Display | `.ml-freq-display` | Subspace comm frequency allocation |
| Schematic | `.ml-schematic` | SVG ship diagram with status zone overlays |
| Mission Clock | `.ml-mission-clock` | Large cinematic countdown/timer |
| Cargo Grid | `.ml-cargo-grid` | Container inventory visualization |

---

## Animation System

### Entrance Animations

| Class | Effect | Duration |
|-------|--------|----------|
| `.ml-animate-fade` | Fade in | 300ms |
| `.ml-animate-up` | Slide up + fade | 300ms |
| `.ml-animate-down` | Slide down + fade | 300ms |
| `.ml-animate-right` | Slide right + fade | 300ms |
| `.ml-animate-left` | Slide left + fade | 300ms |
| `.ml-animate-scale` | Scale in from 0.95 | 300ms |
| `.ml-animate-bounce` | Spring bounce in | 600ms |
| `.ml-animate-power-up` | Clip-path left-to-right reveal | 600ms |
| `.ml-animate-transporter` | Blur + brightness materialization | 1200ms |
| `.ml-animate-viewscreen` | CRT-style horizontal-then-vertical reveal | 800ms |
| `.ml-animate-iris-open` | Circular clip-path reveal | 1000ms |
| `.ml-animate-segment` | ScaleX reveal for LCARS bars | 600ms |

### Ambient Animations

| Class | Effect | Cycle |
|-------|--------|-------|
| `.ml-animate-pulse` | Amber glow pulse | 2s |
| `.ml-animate-pulse-ice` | Ice glow pulse | 2s |
| `.ml-animate-blink` | Opacity blink | 1.5s |
| `.ml-animate-spin` | 360° rotation | 1s |
| `.ml-animate-breathe` | Subtle opacity breathing | 3s |
| `.ml-animate-klaxon` | Red alert background flash | 2s |

### Decorative Effects

| Class | Effect |
|-------|--------|
| `.ml-scanner` | Scanning line sweeps vertically across container |
| `.ml-holo` | Holographic conic gradient shimmer overlay |
| `.ml-energy-flow` | Horizontal light pulse along a bar |
| `.ml-data-cascade` | Vertical data stream background |
| `.ml-warp-streaks` | Horizontal light streaks (activate with `.active`) |

### Staggered Entrance

```html
<div class="ml-stagger">
  <div class="ml-animate-up">First (0ms delay)</div>
  <div class="ml-animate-up">Second (60ms delay)</div>
  <div class="ml-animate-up">Third (120ms delay)</div>
</div>
```

Use `.ml-stagger--fast` for tighter 30ms delays.

### Boot Sequence

```html
<div class="ml-animate-boot">
  <div>LCARS INTERFACE LOADING...</div>
  <div>INITIALIZING SUBSYSTEMS...</div>
  <div>ALL SYSTEMS NOMINAL</div>
</div>
```

### Accessibility

All animations respect `prefers-reduced-motion: reduce`. When enabled, animations are disabled and transitions are instantaneous.

---

## Condition System

Apply alert states to the entire interface via `data-condition` on `<body>`:

```html
<body data-condition="green">  <!-- Normal operations -->
<body data-condition="yellow"> <!-- Elevated alert -->
<body data-condition="red">    <!-- Red alert -->
```

Each condition automatically adjusts:
- Header pill and border colors
- Background ambient gradients
- Glass border tint
- Primary color override (red alert)
- Panel glow intensity
- Sidebar block animations (red alert flashing)

Use `.ml-condition-badge` for an auto-colored status indicator that tracks the current condition.

---

## Layout System

### App Shell

```html
<div class="ml-app">
  <div class="ml-app__sidebar">
    <div class="ml-sidebar"><!-- blocks --></div>
  </div>
  <div class="ml-app__main">
    <div class="ml-header"><!-- header --></div>
    <div class="ml-app__content"><!-- content --></div>
  </div>
</div>
```

### Grid

| Class | Columns |
|-------|---------|
| `.ml-grid--2` | 2 equal columns |
| `.ml-grid--3` | 3 equal columns |
| `.ml-grid--4` | 4 equal columns |
| `.ml-grid--auto` | Auto-fit, min 280px |
| `.ml-grid--auto-sm` | Auto-fit, min 200px |
| `.ml-grid--auto-lg` | Auto-fit, min 360px |

Column spans: `.ml-col-span-2`, `.ml-col-span-3`, `.ml-col-full`

### Responsive Breakpoints

- **1024px** — 4-col grids collapse to 2-col
- **768px** — All grids collapse to 1-col, sidebar becomes horizontal, padding reduces

### Utilities

Flex: `.ml-flex`, `.ml-flex-col`, `.ml-items-center`, `.ml-justify-between`, etc.
Spacing: `.ml-p-{size}`, `.ml-m-{size}`, `.ml-gap-{size}`
Display: `.ml-hidden`, `.ml-block`, `.ml-truncate`
Scroll: `.ml-scroll` (thin styled scrollbar)

---

## Assets

SVG building blocks in `src/assets/`:

- `elbow-top-left.svg` — Top-left elbow connector
- `elbow-bottom-left.svg` — Bottom-left elbow connector
- `pill.svg` — Rounded pill shape

These SVGs can be used as `<img>` tags, CSS `background-image`, or inline SVG for maximum control over color via CSS custom properties.

---

## Theming

### Per-Section Theming

Override tokens on any container to re-theme a section:

```css
.engineering-console {
  --ml-primary: var(--ml-gold);
  --ml-glass-border: rgba(233, 196, 106, 0.12);
}

.medical-console {
  --ml-primary: var(--ml-mint);
  --ml-glass-border: rgba(128, 255, 219, 0.12);
}
```

### Panel Accents

Every panel supports `data-accent` for a colored left border:

```html
<div class="ml-panel" data-accent="amber">Command panel</div>
<div class="ml-panel" data-accent="ice">Tactical panel</div>
<div class="ml-panel" data-accent="mint">Medical panel</div>
```

Available accents: `amber`, `ice`, `violet`, `cyan`, `coral`, `mint`, `gold`, `magenta`

---

## Browser Support

- Chrome/Edge 88+
- Firefox 78+
- Safari 15+

Requires support for: CSS custom properties, `backdrop-filter`, `clip-path`, CSS Grid, `gap` in flexbox.

---

## Contributing

1. Fork the repository
2. Create a feature branch
3. Follow the existing naming conventions (`ml-` prefix, BEM structure)
4. Test across all example screens
5. Submit a pull request

### Naming Convention

- **Blocks:** `.ml-{component}`
- **Elements:** `.ml-{component}__{element}`
- **Modifiers:** `.ml-{component}--{modifier}`
- **States:** `[data-{state}]` attributes or `.active`/`.disabled` classes
- **Utilities:** `.ml-{property}-{value}`
- **Tokens:** `--ml-{category}-{name}`

---

## License

MIT
