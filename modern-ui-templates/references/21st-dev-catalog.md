# 21st.dev Component Catalog & Design Engineering Reference

This reference documents key UI modules, authors, and patterns from **21st.dev** ("The npm for Design Engineers").

---

## 1. Top Authors & Signature Styles

### `@ibelick` (Julien Thibeaut)
* **Dock**: Animated macOS-style dock with magnification on hover, built with Framer Motion spring physics.
* **Magnetic Button**: Interactive button that follows cursor proximity.
* **Minimalist Card**: Clean glassmorphic cards with subtle hover borders.
* **Dynamic Background**: Radial glows, grainy noise layers, and smooth lighting.
* *CLI Installation*: `npx shadcn@latest add "https://21st.dev/r/ibelick/dock"`

### `Origin UI` (originui.com)
* **Interactive Dialogs & Modals**: Multi-step onboarding wizards, confirmation dialogs with rich states.
* **Advanced Inputs**: Pin codes, phone numbers, search bars with keyboard shortcuts (`Cmd+K`), tags inputs.
* **Accessible Form Elements**: Built directly on top of `@radix-ui/react-*` primitives and Tailwind CSS.
* *CLI Installation*: `npx shadcn@latest add "https://21st.dev/r/originui/[component]"`

### `Magic UI` & `Aceternity UI`
* **Animated Beams**: Glowing connector lines between nodes/cards.
* **Bento Grid**: Irregular grid layout highlighting features with integrated icons and hover spotlights.
* **Marquee / Logo Ticker**: Infinite smooth horizontal ticker.
* **3D Pin Card**: Card with perspective tilt and animated pin/radar pulse.

---

## 2. Key Modules & Layout Patterns

### A. Pricing Matrices ("Simple, Transparent Pricing")
* Switch for Monthly vs. Annual billing with discount badges (e.g. "-20%").
* 3-4 tier cards (Free, Basic, Team, Enterprise).
* Highlighted tier: Gradient border, glow backdrop, prominent CTA button.
* Feature list with check/cross icons and tooltips.

### B. Interactive Selectors & Accordion Galleries ("Escape in Style" / "Gourmet Burgers")
* Multi-panel horizontal accordion or tabbed selector.
* Smooth expansion on click or hover: active panel expands (`flex-[3]`), inactive panels shrink (`flex-[1]`).
* Image background with text overlay and micro-badges.

### C. Docks & Floating Navigation
* Bottom-docked or top-docked pill with backdrop-blur.
* Spring-animated magnification when hovering over icons.
* Tooltips positioned dynamically above the hovered dock item.

### D. Gallery Shots Collection
* Masonry or dynamic grid showing interactive thumbnail previews with lightbox modal support.

---

## 3. Tech Stack Conventions
* **React / Next.js**: Functional components with `"use client"` where interactive hooks are required.
* **Styling**: Tailwind CSS (v3 / v4) with `clsx` and `tailwind-merge`.
* **Motion**: `framer-motion` or `motion/react` with spring physics.
* **Icons**: `lucide-react`.
* **Primitives**: `@radix-ui/react-*` (dialog, dropdown-menu, tooltip, slider, tabs).
