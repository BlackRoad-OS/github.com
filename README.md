# BlackRoad — Design System

A minimal, black-background design system built with zero dependencies — pure HTML and CSS. Monospace typography, grid layouts, and white-border separators throughout.

## Pages

| File             | Description                                           |
|------------------|-------------------------------------------------------|
| `index.html`     | Animation Dictionary — 17 CSS animation primitives    |
| `library.html`   | Mobile SDK — packages, install, platforms, changelog   |
| `directory.html` | Infrastructure Index — enterprise, orgs, domains       |

---

## Animation Dictionary (`index.html`)

17 CSS animation primitives with the BlackRoad color palette. Shapes move in color, text stays white or black.

```
┌──────────────────────────────────────────────────────────────────────┐
│  BlackRoad                              motion   colors   docs       │
├══════════════════════════════════════════════════════════════════════┤
│  ▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬  (gradient rule)                    │
├──────────────────────────────────────────────────────────────────────┤
│  ANIMATION DICTIONARY V1.0                                           │
│                                                                      │
│  Motion                                                              │
│  Index                                                               │
│                                                                      │
│  Shapes move in color. Text stays white or black.                    │
│  ▬▬▬▬▬▬▬▬▬▬  (brand rule)                                           │
├──────────────────────────────────────────────────────────────────────┤
│  PALETTE  ● #FF8400  ● #FF4400  ● #FF0066  ● #CC00AA               │
│           ● #8800FF  ● #0066FF  ● #2233CC    text → #fff/#000 only  │
├──────────────────────┬──────────────────────┬────────────────────────┤
│  01 ─────────────    │  02 ─────────────    │  03 ────────────       │
│  ┌────────────────┐  │  ┌────────────────┐  │  ┌──────────────┐     │
│  │   ● fade       │  │  │  ●→  slide-x   │  │  │  ● slide-y   │     │
│  └────────────────┘  │  └────────────────┘  │  └──────────────┘     │
│  fade · 2s           │  slide-x · 2s        │  slide-y · 2s         │
├──────────────────────┼──────────────────────┼────────────────────────┤
│  04 ─────────────    │  05 ─────────────    │  06 ────────────       │
│  ┌────────────────┐  │  ┌────────────────┐  │  ┌──────────────┐     │
│  │  (●) pulse     │  │  │   ◻ spin       │  │  │  ● blink     │     │
│  └────────────────┘  │  └────────────────┘  │  └──────────────┘     │
│  pulse · 1.5s        │  spin · 2s           │  blink · 1s           │
├──────────────────────┼──────────────────────┼────────────────────────┤
│  07 ─────────────    │  08 ─────────────    │  09 ────────────       │
│  ┌────────────────┐  │  ┌────────────────┐  │  ┌──────────────┐     │
│  │  ● bounce ↑↓   │  │  │  ━━━━ grow     │  │  │  ←●→ shake   │     │
│  └────────────────┘  │  └────────────────┘  │  └──────────────┘     │
│  bounce · 1s         │  grow · 2s           │  shake · 1s           │
├──────────────────────┼──────────────────────┼────────────────────────┤
│  10 ─────────────    │  11 ─────────────    │  12 ────────────       │
│  ┌────────────────┐  │  ┌────────────────┐  │  ┌──────────────┐     │
│  │  · ● orbit     │  │  │  blackroad▌    │  │  │  ▎▎▎▎▎ wave  │     │
│  └────────────────┘  │  └────────────────┘  │  └──────────────┘     │
│  orbit · 2s          │  cursor · 0.8s       │  wave · 1s            │
├──────────────────────┼──────────────────────┼────────────────────────┤
│  13 ─────────────    │  14 ─────────────    │  15 ────────────       │
│  ┌────────────────┐  │  ┌────────────────┐  │  ┌──────────────┐     │
│  │   ◻ flip       │  │  │  ● color-cycle │  │  │  ▬▬ grad     │     │
│  └────────────────┘  │  └────────────────┘  │  └──────────────┘     │
│  flip · 2s           │  color-cycle · 3s    │  grad-shift · 3s      │
├──────────────────────┼──────────────────────┼────────────────────────┤
│  16 ─────────────    │  17 ─────────────    │                        │
│  ┌────────────────┐  │  ┌────────────────┐  │                        │
│  │  BlackRoad     │  │  │  ○ border      │  │                        │
│  │  BlackRoad     │  │  │    pulse       │  │                        │
│  │  BlackRoad     │  │  └────────────────┘  │                        │
│  └────────────────┘  │  border-pulse · 2s   │                        │
│  text rule           │                      │                        │
├──────────────────────┴──────────────────────┴────────────────────────┤
│  BlackRoad OS, Inc.       17 primitives · shapes in color            │
└──────────────────────────────────────────────────────────────────────┘
```

### Primitives

| #  | Name         | Property            | Easing       | Duration |
|----|--------------|---------------------|--------------|----------|
| 01 | fade         | opacity             | ease-in-out  | 2s       |
| 02 | slide-x      | translateX          | ease-in-out  | 2s       |
| 03 | slide-y      | translateY          | ease-in-out  | 2s       |
| 04 | pulse        | scale               | ease-in-out  | 1.5s     |
| 05 | spin         | rotate              | linear       | 2s       |
| 06 | blink        | opacity             | step-end     | 1s       |
| 07 | bounce       | translateY          | ease-in-out  | 1s       |
| 08 | grow         | scaleX              | ease-in-out  | 2s       |
| 09 | shake        | translateX          | ease-in-out  | 1s       |
| 10 | orbit        | rotate + translateX | linear       | 2s       |
| 11 | cursor       | opacity             | step-end     | 0.8s     |
| 12 | wave         | scaleY (staggered)  | ease-in-out  | 1s       |
| 13 | flip         | rotateY             | ease-in-out  | 2s       |
| 14 | color-cycle  | background color    | linear       | 3s       |
| 15 | grad-shift   | background position | ease         | 3s       |
| 16 | text rule    | (static reference)  | —            | —        |
| 17 | border-pulse | border-color        | ease-in-out  | 2s       |

### Color Palette

| Swatch   | Hex       |
|----------|-----------|
| Orange   | `#FF8400` |
| Red      | `#FF4400` |
| Pink     | `#FF0066` |
| Magenta  | `#CC00AA` |
| Purple   | `#8800FF` |
| Blue     | `#0066FF` |
| Navy     | `#2233CC` |

---

## Mobile SDK Library (`library.html`)

Package registry, install commands, platform support, and changelog.

```
┌──────────────────────────────────────────────────────────────────────┐
│  BlackRoad                       packages  install  platforms  docs   │
├──────────────────────────────────────────────────────────────────────┤
│  LIBRARY V0.4.2                                                      │
│                                                                      │
│  Mobile                                                              │
│  SDK                                                                 │
│                                                                      │
│  ┌─────────┐ ┌──────────────────────┐ ┌─────────┐ ┌────────────┐    │
│  │ v 0.4.2 │ │ iOS · Android · RN   │ │   MIT   │ │ 8 packages │    │
│  └─────────┘ └──────────────────────┘ └─────────┘ └────────────┘    │
├──────────────────────┬──────────────────────┬────────────────────────┤
│  PACKAGES · 8        │  INSTALL             │  PLATFORMS             │
│                      │                      │                        │
│  @blackroad/core     │  $ npm install       │  █ iOS       ≥ 16.0   │
│  @blackroad/agents   │    @blackroad/core   │  █ Android   API 26+  │
│  @blackroad/ui       │                      │  █ React Native ≥0.72 │
│  @blackroad/memory   │  $ yarn add          │  █ Expo      SDK 50+  │
│  @blackroad/network  │    @blackroad/core   │  ░ macOS     exp.     │
│  @blackroad/crypto   │                      │  ░ tvOS      planned  │
│  @blackroad/inference│  $ pnpm add          │  ░ watchOS   n/a      │
│  @blackroad/telemetry│    @blackroad/core   │                        │
│                      │                      │  CHANGELOG             │
│                      │  PEER DEPS           │  0.4.2 · memory fix   │
│                      │  react-native ≥0.72  │  0.4.1 · UI tokens    │
│                      │  react ≥18.0         │  0.4.0 · NATS+mesh   │
│                      │  @nats-io (opt)      │  0.3.9 · PS-SHA∞     │
│                      │                      │  0.3.0 · initial      │
├──────────────────────┴──────────────────────┴────────────────────────┤
│  BlackRoad OS, Inc.           8 packages · 4 platforms · MIT         │
└──────────────────────────────────────────────────────────────────────┘
```

### Packages

| Package               | Version | Size  |
|-----------------------|---------|-------|
| `@blackroad/core`      | 0.4.2   | 12kb  |
| `@blackroad/agents`    | 0.4.2   | 18kb  |
| `@blackroad/ui`        | 0.4.1   | 34kb  |
| `@blackroad/memory`    | 0.3.9   | 9kb   |
| `@blackroad/network`   | 0.4.0   | 22kb  |
| `@blackroad/crypto`    | 0.4.2   | 7kb   |
| `@blackroad/inference`  | 0.2.1   | 41kb  |
| `@blackroad/telemetry` | 0.4.2   | 11kb  |

---

## Infrastructure Directory (`directory.html`)

GitHub enterprise, organizations, and registered domains.

```
┌──────────────────────────────────────────────────────────────────────┐
│  BlackRoad                       enterprise  orgs  domains  docs     │
├──────────────────────────────────────────────────────────────────────┤
│  DIRECTORY V1.0                                                      │
│                                                                      │
│  Infrastructure                                                      │
│  Index                                                               │
│                                                                      │
│  GitHub enterprise, organizations, and registered domains.           │
├──────────────────────┬──────────────────────┬────────────────────────┤
│  GITHUB ENTERPRISE   │  ORGANIZATIONS · 15  │  DOMAINS · 19         │
│                      │                      │                        │
│  ┌────────────────┐  │  Blackbox-Enterprises │  — blackboxprogramming│
│  │  blackroad-os  │  │  BlackRoad-AI        ↗│  — blackroad.company  │
│  │  github.com/   │  │  BlackRoad-Archive   ↗│  — blackroad.io       │
│  │  enterprises/  │  │  BlackRoad-Cloud     ↗│  — blackroad.me       │
│  │  blackroad-os  │  │  BlackRoad-Education ↗│  — blackroad.network  │
│  └────────────────┘  │  BlackRoad-Foundation↗│  — blackroad.systems  │
│                      │  BlackRoad-Gov       ↗│  — blackroadai.com    │
│                      │  BlackRoad-Hardware  ↗│  — blackroadinc.us    │
│                      │  BlackRoad-Interactive↗│  — blackroadqi.com    │
│                      │  BlackRoad-Labs      ↗│  — blackroadquantum.* │
│                      │  BlackRoad-Media     ↗│  — lucidia.earth      │
│                      │  BlackRoad-OS        ↗│  — lucidia.studio     │
│                      │  BlackRoad-Security  ↗│  — lucidiaqi.com      │
│                      │  BlackRoad-Studio    ↗│  — roadchain.io       │
│                      │  BlackRoad-Ventures  ↗│  — roadcoin.io        │
├──────────────────────┴──────────────────────┴────────────────────────┤
│  BlackRoad OS, Inc.         1 enterprise · 15 orgs · 19 domains      │
└──────────────────────────────────────────────────────────────────────┘
```

### Organizations

| Organization            | Link                                          |
|-------------------------|-----------------------------------------------|
| Blackbox-Enterprises    | github.com/Blackbox-Enterprises               |
| BlackRoad-AI            | github.com/BlackRoad-AI                       |
| BlackRoad-Archive       | github.com/BlackRoad-Archive                  |
| BlackRoad-Cloud         | github.com/BlackRoad-Cloud                    |
| BlackRoad-Education     | github.com/BlackRoad-Education                |
| BlackRoad-Foundation    | github.com/BlackRoad-Foundation               |
| BlackRoad-Gov           | github.com/BlackRoad-Gov                      |
| BlackRoad-Hardware      | github.com/BlackRoad-Hardware                 |
| BlackRoad-Interactive   | github.com/BlackRoad-Interactive              |
| BlackRoad-Labs          | github.com/BlackRoad-Labs                     |
| BlackRoad-Media         | github.com/BlackRoad-Media                    |
| BlackRoad-OS            | github.com/BlackRoad-OS                       |
| BlackRoad-Security      | github.com/BlackRoad-Security                 |
| BlackRoad-Studio        | github.com/BlackRoad-Studio                   |
| BlackRoad-Ventures      | github.com/BlackRoad-Ventures                 |

### Domains

```
blackboxprogramming.io    blackroad.company       blackroad.io
blackroad.me              blackroad.network       blackroad.systems
blackroadai.com           blackroadinc.us         blackroadqi.com
blackroadquantum.com      blackroadquantum.info   blackroadquantum.net
blackroadquantum.shop     blackroadquantum.store  lucidia.earth
lucidia.studio            lucidiaqi.com           roadchain.io
roadcoin.io
```

---

## Stack

- **HTML** — semantic markup, zero frameworks
- **CSS** — `@keyframes`, CSS custom properties, grid layout
- **Font** — JetBrains Mono (Google Fonts)

## Usage

Open any `.html` file in a modern browser. No build step required.

```
git clone <repo-url>
open index.html
open library.html
open directory.html
```

## Design Principles

- Pure black `#000000` background
- Monospace typography (JetBrains Mono)
- Grid layout with white border separators
- Responsive: 1-col mobile, 2-col tablet, 3-col desktop
- Shapes animate in brand colors; text stays strictly `#ffffff` / `#000000`

## License

See [LICENSE](LICENSE) for details.
