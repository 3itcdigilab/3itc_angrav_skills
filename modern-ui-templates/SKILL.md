---
name: modern-ui-templates
description: "Extract, adapt, and implement modern UI/UX components, templates, and design systems from websites, design registries (21st.dev, React Bits, Magic UI, Aceternity, Origin UI, ibelick), or screenshots into production React, Next.js, and Tailwind CSS code."
---

# Modern UI Templates & Web UI Extractor

This skill equips the agent to extract, reverse-engineer, and implement high-grade UI/UX components and templates from design libraries like **React Bits**, **21st.dev**, and **live external websites**.

---

## 1. Quick Reference: Core Sources

| Source | Specialty | How to Ingest / Install |
| :--- | :--- | :--- |
| **React Bits** (`reactbits.dev`) | Interactive animations, text effects, canvas/WebGL/CSS backgrounds, cursors, cards | `npx shadcn@latest add @react-bits/[ComponentName]-TS-TW` or pull from `DavidHDev/react-bits` GitHub |
| **21st.dev** (`21st.dev`) | "The npm for Design Engineers" — community shadcn components (ibelick, Origin UI, Magic UI, Aceternity UI, Kokonut UI) | `npx shadcn@latest add "https://21st.dev/r/[author]/[component]"` or reconstruct via shadcn/Radix/Tailwind |
| **Live Websites & Screenshots** | Reverse-engineering any live website into clean reusable code | Extract tokens (colors, typography, radii, shadows) -> Deconstruct layout -> Build with Tailwind + Motion |

---

## 2. React Bits Integration (`reactbits.dev`)

React Bits provides 165+ animated, interactive components created by David Haz for React + Tailwind / CSS.

### 2.1 Component Categories

#### Text Animations
* `BlurText`: Blur reveal animation on load or scroll.
* `SplitText`: Character/word stagger animation.
* `ShinyText`: Smooth shimmering gradient effect across text.
* `DecryptedText`: Cyberpunk-style letter decoding effect.
* `TrueFocus`: Spotlight/focus blur on active word.
* `VariableProximity`: Dynamic weight/style based on cursor distance.
* `GlitchText`: Glitch distortion on hover or loop.
* `CountUp`: Animated numerical counter with spring physics.
* `ScrollVelocity`: Infinite text marquee with scroll speed acceleration.
* `RotatingText`: Flipping text cycler for hero headlines.

#### Animations & Micro-interactions
* `BlobCursor`, `GhostCursor`, `SplashCursor`, `FollowCursor`: Interactive cursor effects.
* `Magnet`: Button or element magnetically pulled toward mouse cursor.
* `SpotlightCard`, `PixelCard`, `TiltCard`, `DecayCard`: Modern interactive cards with hover tracking.
* `StarBorder`, `ElectricBorder`: Animated border glowing lines.
* `ClickSpark`: Particle burst upon user click.

#### Backgrounds
* `Aurora`: Multi-color flowing northern lights background.
* `Hyperspeed`: Warp speed light streaks.
* `Balatro`: Trippy animated shader background.
* `Particles` & `DotGrid`: Interactive particle / dot mesh backgrounds.
* `Waves` & `SlicedWaves`: Elegant wavy lines with dynamic flow.
* `GridDistortion`: Interactive cursor-responsive grid mesh.

#### Components & Navigation
* `Dock`: Apple-style magnifying dock with spring physics.
* `Stack`: Swipable / flickable card stack.
* `ElasticSlider`: Elastic drag-responsive slider.
* `CircularGallery`: 3D cylinder rotating image gallery.
* `MagicBento`: Interactive bento layout with glowing borders.
* `CardNav` / `FlowingMenu`: Creative menu and navigation patterns.

### 2.2 React Bits Usage & Installation
To install via shadcn CLI:
```bash
npx shadcn@latest add @react-bits/ComponentName-TS-TW
```
Variants:
* `-TS-TW`: TypeScript + Tailwind CSS (Recommended)
* `-JS-TW`: JavaScript + Tailwind CSS
* `-TS-CSS`: TypeScript + Vanilla CSS
* `-JS-CSS`: JavaScript + Vanilla CSS

Raw Source Repository:
`https://raw.githubusercontent.com/DavidHDev/react-bits/main/src/content/[Category]/[ComponentName]/[ComponentName].[jsx|tsx]`

---

## 3. 21st.dev Integration (`21st.dev`)

21st.dev is the community registry for shadcn-compatible design engineering.

### 3.1 Top Authors & Key Patterns
* **`@ibelick` (Julien Thibeaut)**:
  - macOS Dock (`@ibelick/dock`)
  - Magnetic Button (`@ibelick/magnetic-button`)
  - Minimalist hover cards and dynamic radial backgrounds
* **`Origin UI`**:
  - Interactive multi-step dialogs / onboarding wizards
  - Accessible custom selects, sliders, inputs, and toggles
* **`Magic UI`**:
  - Bento grids, Marquee tickers, Interactive beams, Border beams
* **`Aceternity UI`**:
  - 3D card perspective, Lamp header effect, Canvas reveal effect
* **`Community Modules`**:
  - Pricing Tables (Monthly/Annual switch, tiered highlights)
  - Interactive Selectors / Accordion Galleries (e.g. Mountain Spa / Escape in Style)
  - Hero headers with animated badge pills and subtle radial glow

### 3.2 Installation Command
```bash
npx shadcn@latest add "https://21st.dev/r/[author]/[component]"
```
*Example:*
```bash
npx shadcn@latest add "https://21st.dev/r/ibelick/dock"
```

---

## 4. Universal Website Reverse-Engineering Workflow

When the user shares a website URL or screenshot to borrow/replicate:

```
[Target Website / Screenshot]
         │
         ▼
[1. Design Tokens] ────► Colors, Fonts, Border Radii, Backdrop Blurs, Shadows
         │
         ▼
[2. Layout Structure] ─► Header/Dock, Hero, Bento Grid, Showcase, Pricing, Footer
         │
         ▼
[3. Micro-Interactions] ─► Hover physics, Magnetic pull, Spring transitions, Scroll triggers
         │
         ▼
[4. Code Generation] ──► Next.js / React + Tailwind CSS + Framer Motion + Lucide Icons
```

### Step 1: Design Token Extraction
1. **Color System**:
   - Dark theme base: `bg-zinc-950`, `bg-[#0a0a0c]`, `bg-black/90`
   - Border tones: `border-white/10`, `border-zinc-800`
   - Accents: Vibrant gradients (e.g. `from-violet-600 via-indigo-600 to-cyan-500`)
   - Text contrast: Primary `text-zinc-100`, Secondary `text-zinc-400`, Muted `text-zinc-600`
2. **Glassmorphism**:
   - `backdrop-blur-xl bg-white/5 border border-white/10 shadow-2xl`
3. **Typography**:
   - Headers: `tracking-tight font-semibold text-balance`
   - Body: `leading-relaxed text-zinc-400`

### Step 2: Component Architecture
Always output modular, readable components:
* Keep subcomponents clean and decoupled.
* Standardize on Lucide icons (`lucide-react`).
* Use `cn()` helper (`clsx` + `tailwind-merge`) for flexible class overrides.
* Use `motion` from `framer-motion` (or `motion/react`) for silky physics.

---

## 5. Production Reference Components

### 5.1 Interactive Magnifying Dock
```tsx
"use client";

import React, { useRef } from "react";
import { motion, useMotionValue, useSpring, useTransform } from "framer-motion";

interface DockItemProps {
  icon: React.ReactNode;
  label: string;
  onClick?: () => void;
}

export function Dock({ items }: { items: DockItemProps[] }) {
  const mouseX = useMotionValue(Infinity);

  return (
    <motion.div
      onMouseMove={(e) => mouseX.set(e.pageX)}
      onMouseLeave={() => mouseX.set(Infinity)}
      className="fixed bottom-6 left-1/2 -translate-x-1/2 flex h-16 items-end gap-3 rounded-full border border-white/10 bg-neutral-900/80 px-4 pb-3 shadow-2xl backdrop-blur-xl z-50"
    >
      {items.map((item, i) => (
        <DockIcon key={i} mouseX={mouseX} item={item} />
      ))}
    </motion.div>
  );
}

function DockIcon({ mouseX, item }: { mouseX: any; item: DockItemProps }) {
  const ref = useRef<HTMLDivElement>(null);
  const distance = useTransform(mouseX, (val: number) => {
    const bounds = ref.current?.getBoundingClientRect() ?? { x: 0, width: 0 };
    return val - bounds.x - bounds.width / 2;
  });

  const widthSync = useTransform(distance, [-120, 0, 120], [42, 68, 42]);
  const width = useSpring(widthSync, { mass: 0.1, stiffness: 180, damping: 14 });

  return (
    <motion.div
      ref={ref}
      style={{ width, height: width }}
      onClick={item.onClick}
      className="group relative flex aspect-square cursor-pointer items-center justify-center rounded-full bg-neutral-800/90 text-neutral-200 shadow-lg hover:bg-neutral-700/90 transition-colors"
    >
      <span className="text-xl">{item.icon}</span>
      <span className="pointer-events-none absolute -top-9 rounded-lg bg-neutral-950 border border-white/10 px-2.5 py-1 text-xs font-medium text-neutral-200 opacity-0 shadow-xl transition-opacity group-hover:opacity-100 whitespace-nowrap">
        {item.label}
      </span>
    </motion.div>
  );
}
```

### 5.2 Interactive Bento Grid Card with Hover Spotlight
```tsx
"use client";

import React, { useRef, useState } from "react";

export function SpotlightCard({
  children,
  className = "",
  spotlightColor = "rgba(139, 92, 246, 0.15)",
}: {
  children: React.ReactNode;
  className?: string;
  spotlightColor?: string;
}) {
  const divRef = useRef<HTMLDivElement>(null);
  const [position, setPosition] = useState({ x: 0, y: 0 });
  const [opacity, setOpacity] = useState(0);

  const handleMouseMove = (e: React.MouseEvent<HTMLDivElement>) => {
    if (!divRef.current) return;
    const rect = divRef.current.getBoundingClientRect();
    setPosition({ x: e.clientX - rect.left, y: e.clientY - rect.top });
  };

  return (
    <div
      ref={divRef}
      onMouseMove={handleMouseMove}
      onMouseEnter={() => setOpacity(1)}
      onMouseLeave={() => setOpacity(0)}
      className={`relative overflow-hidden rounded-3xl border border-neutral-800 bg-neutral-900/50 p-6 backdrop-blur-sm transition-all duration-300 hover:border-neutral-700 ${className}`}
    >
      <div
        className="pointer-events-none absolute -inset-px transition-opacity duration-300"
        style={{
          opacity,
          background: `radial-gradient(600px circle at ${position.x}px ${position.y}px, ${spotlightColor}, transparent 40%)`,
        }}
      />
      <div className="relative z-10">{children}</div>
    </div>
  );
}
```

---

## 6. How the Agent Applies This Skill

When the user asks to build or replicate a UI:
1. Identify the visual aesthetic and component pattern from the source URL or screenshot.
2. Recommend the best matching components from **React Bits** (animations, effects) and **21st.dev** (UI modules, blocks, cards).
3. Provide the ready-to-run installation CLI command or generate the complete, self-contained TSX component code immediately.
