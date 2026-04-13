# Design System Strategy: High-Tech Editorial for QDAY Network

## 1. Overview & Creative North Star: "The Quantum Obsidian"
This design system is engineered to move beyond the "standard" blockchain aesthetic of flat grids and predictable neon lines. Our Creative North Star is **The Quantum Obsidian**: a visual language that feels heavy, permanent, and premium, yet is sliced by light and ethereal layers of digital intelligence.

We break the "template" look through **Kinetic Asymmetry**. Instead of rigid columns, elements should feel like they are floating in a deep-space vacuum, anchored by intentional overlaps and high-contrast typography scales. We prioritize the "Editorial High-End" experience—treating information not just as data, but as a curated exhibition of the future.

## 2. Colors & Atmospheric Depth
The palette is rooted in the `background` (#0b0e14), a deep charcoal that serves as our infinite canvas.

*   **Primary & Secondary Fusion:** We use `primary` (#a4a6ff) and `secondary` (#b387ff) not just as flat fills, but as light sources. These colors represent the "Quantum Glow" within the Obsidian environment.
*   **The "No-Line" Rule:** To maintain a premium feel, **1px solid borders are prohibited for sectioning.** Boundaries must be defined solely through background shifts. For example, a `surface-container-low` section sitting directly on a `surface` background creates a sophisticated, seamless transition.
*   **Surface Hierarchy & Nesting:** Use the surface-container tiers to create structural importance. 
    *   `surface-container-lowest` (#000000): Use for "sunken" utility areas or the deep footer.
    *   `surface-container-highest` (#22262f): Use for the most prominent interactive cards.
*   **The "Glass & Gradient" Rule:** Floating UI elements (like navigation bars or hovering data cards) must utilize **Glassmorphism**. Combine `surface-variant` at 60% opacity with a `backdrop-blur` of 20px. 
*   **Signature Textures:** Apply linear gradients from `primary` to `primary-dim` for high-impact CTAs. This creates a "3D light-bar" effect that feels tactile and energized.

## 3. Typography: The Authoritative Voice
Our typography balance pairs the technical precision of **Inter** with the futuristic, wide-set character of **Space Grotesk**.

*   **Display & Headlines (Space Grotesk):** Large-scale headlines (`display-lg` at 3.5rem) should feel like architectural statements. Use tight letter-spacing (-0.02em) to give the brand an "expensive" editorial weight.
*   **Body & Titles (Inter):** Inter provides the functional clarity required for complex blockchain concepts. Use `body-lg` (1rem) for general copy to ensure it doesn't feel "cramped" against the large headlines.
*   **Labels (Manrope):** For micro-copy and metadata, Manrope offers a modern, slightly technical flair that distinguishes "system data" from "brand storytelling."
*   **Hierarchy Note:** Always lead with high contrast. A `display-lg` in `on_surface` should be followed by a `body-lg` in `on_surface_variant` to create a clear visual path through the narrative.

## 4. Elevation & Depth: Tonal Layering
In this system, depth is a result of light and shadow, not lines.

*   **The Layering Principle:** Rather than shadows, use "stacking." Place a `surface-container-high` card on a `surface-container` background. The subtle 2-3% shift in luminosity provides all the "lift" needed for a high-end interface.
*   **Ambient Shadows:** When a true "floating" state is required (e.g., a modal or dropdown), use a massive blur (40px-80px) at a very low 6% opacity. The shadow color must be a tinted version of `on-surface` (#ecedf6) to simulate light passing through glass, rather than a muddy black.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, it must be a **Ghost Border**. Use the `outline-variant` token at 15% opacity. It should be "felt" rather than "seen."
*   **Luminous Glows:** Use `tertiary_container` (#00e3fd) as a background "blob" or "aura" behind key components to simulate the bioluminescence of a quantum network.

## 5. Components: The Primitive Set

### Buttons
*   **Primary:** A gradient-filled container (`primary` to `primary_dim`) with `on_primary_container` text. Use `rounded-md` (0.375rem).
*   **Secondary:** Ghost-style. No fill, with a `primary` Ghost Border (20% opacity) and `primary` text.
*   **Interaction:** On hover, the primary button should emit a soft outer glow using the `surface_tint` color.

### Cards & Containers
*   **The Rule:** **Forbid the use of divider lines.** Use vertical whitespace from the spacing scale (e.g., 48px or 64px) to separate content clusters.
*   **Styling:** Cards should use `surface_container_low` with a subtle `backdrop-blur` if they overlap a gradient background.

### Input Fields
*   **Base:** `surface_container_highest` background with a `none` border.
*   **Active State:** A 1px Ghost Border using `primary` at 40% opacity and a subtle `primary` glow.

### Additional Signature Component: The "Quantum Bridge" Timeline
*   For the roadmap or network stats, use a horizontal line that fades in and out using a gradient (`transparent` -> `primary` -> `transparent`). Nodes should be `tertiary` glows that pulse slightly.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts where one side of the screen has a large `display-lg` heading and the other has a high-detail `surface-container` card.
*   **Do** lean into "Breathing Room." High-end design requires negative space to let the colors and gradients feel intentional.
*   **Do** use `tertiary` (#81ecff) sparingly as a "data accent" to highlight critical numbers or "Active" states.

### Don't:
*   **Don't** use 100% white (#ffffff). Always use `on_surface` (#ecedf6) to avoid harsh optical vibration against the dark background.
*   **Don't** use standard "drop shadows" on text. It cheapens the "Quantum Obsidian" look. Rely on high color contrast for legibility.
*   **Don't** use sharp corners. Use the `rounded-lg` (0.5rem) and `rounded-xl` (0.75rem) tokens to keep the futuristic feel approachable and "liquid."