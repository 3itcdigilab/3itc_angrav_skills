# React Bits Complete Component Catalog

Created by David Haz ([reactbits.dev](https://reactbits.dev) & [github.com/DavidHDev/react-bits](https://github.com/DavidHDev/react-bits)).

---

## 1. Text Animations (32 Components)
* **ASCIIText**: ASCII art rendering of typography with canvas.
* **BlurText**: Progressive letter/word blur-in on load or viewport enter.
* **CircularText**: Text wrapped dynamically along a circle radius with continuous rotation.
* **CountUp**: Smooth spring-based counter for numbers and statistics.
* **CurvedLoop**: Text following an SVG curve/path in an infinite loop.
* **DecryptedText**: Hacker/cyberpunk random character scramble that settles on text.
* **DepthText**: 3D parallax depth effect on text layers.
* **EchoText**: Motion trail echo effect behind text on hover.
* **FallingText**: Physics-based gravity dropping effect for text characters.
* **FoldText**: 3D origami paper-folding transition for text.
* **FuzzyText**: Soft chromatic aberration and fuzz effect.
* **GlitchText**: Cybernetic glitch effect with slice offsets.
* **GradientText**: Animated shifting gradient background clipped to text.
* **MaskedHeading**: Video or canvas mask inside large heading typography.
* **ParticleText**: Canvas particle simulation morphing into text characters.
* **RotatingText**: Morphing text rotator for hero headlines (e.g. "Build [Faster, Better, Stronger]").
* **ScrambledText**: Text scrambling on hover or interval.
* **ScrollFloat**: Words floating up as user scrolls down.
* **ScrollReveal**: Opacity and transform reveal driven by scroll position.
* **ScrollVelocity**: Marquee where velocity scales dynamically with scroll speed.
* **ShinyText**: Shimmering light sweep across text.
* **Shuffle**: Randomized letter shuffle transition.
* **SplitFlapText**: Airport departure-board style flip mechanical animation.
* **SplitText**: Character-by-character or word-by-word spring stagger.
* **StrokeText**: Animated SVG stroke-dasharray drawing outline of text.
* **TextCursor**: Typewriter effect with dynamic blinking cursor.
* **TextLoop**: Vertical smooth carousel of keywords.
* **TextPressure**: Variable font weight and width adapting to mouse proximity.
* **TextType**: Natural human typewriter effect with random delay intervals.
* **TrueFocus**: Interactive spotlight that sharpens the hovered word while blurring others.
* **VariableProximity**: Variable font weight responding to mouse distance.
* **WarpText**: Wave or cylindrical distortion on text.

---

## 2. Animations & Micro-Interactions (38 Components)
* **AnimatedContent**: Staggered container entry animations.
* **BlobCursor**: Liquid fluid cursor blob following mouse pointer.
* **ClickSpark**: Multi-particle spark burst radiating from click coordinates.
* **Crosshair**: Subtle targeting reticle tracking cursor movement.
* **Cubes**: Interactive 3D CSS cubes reacting to cursor.
* **ElasticMesh**: Deformable spring mesh on hover.
* **ElectricBorder**: Crackling electric discharge line traveling around borders.
* **FadeContent**: Seamless viewport fade-in helper.
* **GhostCursor**: Ethereal trailing motion ghost effect.
* **GlareHover**: Realistic light glare reflection following pointer over a card.
* **GlowCursor**: Ambient radial light source attached to cursor.
* **GradualBlur**: Progressive depth-of-field blur gradient.
* **ImageTrail**: Trail of images appearing sequentially behind fast cursor motion.
* **LaserFlow**: Sleek glowing laser beam running through card borders.
* **Magnet**: Element magnetically pulled toward cursor with spring release.
* **MagnetLines**: Array of lines rotating to point towards mouse position.
* **MetaBalls**: Gooey metaball physics merging and splitting.
* **PixelCard**: Retro 8-bit pixelated reveal effect on hover.
* **PixelTrail**: Grid of pixels lighting up where cursor moves.
* **Ribbons**: 3D waving ribbons in WebGL/Three.js.
* **SplashCursor**: WebGL fluid simulation with colorful splashes on mouse drag.
* **StarBorder**: Twinkling star path traversing card perimeter.
* **StickerPeel**: Realistic corner peel-off effect with backface shadow.
* **TargetCursor**: Gaming/tactical HUD cursor styling.
* **TiltCard**: 3D perspective card tilt with gyroscope/mouse input.

---

## 3. Backgrounds (56 Components)
* **Aurora**: Northern lights fluid gradient shader.
* **Balatro**: Hypnotic, swirling psychedelic shader inspired by the game Balatro.
* **Ballpit**: 2D/3D physics balls bouncing inside viewport boundary.
* **Beams**: Volumetric light beams shining through mist.
* **DarkVeil**: Dark aesthetic animated noise veil.
* **DotGrid**: Interactive canvas dot matrix with ripple waves on click.
* **GridDistortion**: Wavy warped grid mesh reacting to mouse drag.
* **Hyperspeed**: Sci-fi warp speed starfield/highway streak tunnel.
* **Iridescence**: Soap-bubble chromatic fluid surface.
* **LightRays**: God rays streaming from top of screen.
* **LiquidEther**: Ambient fluid smoke simulation.
* **Orb**: Glowing plasma orb with pulse animations.
* **Particles**: Floating network of interconnected nodes and lines.
* **Squares**: Infinite scrolling grid of perspective squares.
* **Threads**: Elegant moving silky strands.
* **Waves**: Calming sinusoidal wave lines.

---

## 4. Components & Nav (45 Components)
* **AccordionGallery**: Horizontal image accordion expanding active panel.
* **BubbleMenu**: Circular pop-out floating action menu.
* **CardNav**: Tabbed navigation with sliding active indicator.
* **CardSwap**: Interactive card shuffle deck animation.
* **CircularGallery**: 3D cylinder rotating gallery with drag physics.
* **Dock**: macOS-style magnifying dock with smooth spring math.
* **ElasticSlider**: Fluid slider that stretches elastically beyond bounds.
* **InfiniteMenu**: Infinite scrolling circular item picker.
* **MagicBento**: Modular bento grid with dynamic glow and mouse tracking.
* **Masonry**: Responsive staggered layout with enter animations.
* **PillNav**: Minimalist floating pill navbar.
* **PixelCard**: Interactive retro card with pixel grid background.
* **SpotlightCard**: Card with radial spotlight following cursor position.
* **Stack**: Tinder-like swipeable card stack with throw physics.
* **TiltedCard**: Card with realistic 3D depth layers.

---

## 5. Quick CLI Cheat Sheet
```bash
# Text Animations
npx shadcn@latest add @react-bits/BlurText-TS-TW
npx shadcn@latest add @react-bits/SplitText-TS-TW
npx shadcn@latest add @react-bits/ShinyText-TS-TW
npx shadcn@latest add @react-bits/DecryptedText-TS-TW
npx shadcn@latest add @react-bits/TrueFocus-TS-TW

# Animations & Cards
npx shadcn@latest add @react-bits/SpotlightCard-TS-TW
npx shadcn@latest add @react-bits/PixelCard-TS-TW
npx shadcn@latest add @react-bits/TiltCard-TS-TW
npx shadcn@latest add @react-bits/StarBorder-TS-TW
npx shadcn@latest add @react-bits/ClickSpark-TS-TW

# Backgrounds
npx shadcn@latest add @react-bits/Aurora-TS-TW
npx shadcn@latest add @react-bits/Hyperspeed-TS-TW
npx shadcn@latest add @react-bits/Waves-TS-TW
npx shadcn@latest add @react-bits/Particles-TS-TW

# Components
npx shadcn@latest add @react-bits/Dock-TS-TW
npx shadcn@latest add @react-bits/Stack-TS-TW
npx shadcn@latest add @react-bits/CircularGallery-TS-TW
npx shadcn@latest add @react-bits/ElasticSlider-TS-TW
```
