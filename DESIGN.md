# Design System Document: The Eco-Editorial Standard

## 1. Overview & Creative North Star

### Creative North Star: "The Living Archive"
This design system moves away from the rigid, clinical grids of traditional educational software. Instead, it adopts the persona of a "Living Archive"—a high-end editorial experience that feels like a premium nature journal brought to life. We achieve this by blending **Organic Minimalism** with **Asymmetric Sophistication**. 

By utilizing intentional white space (breathing room), overlapping surface layers, and a high-contrast typographic scale, we transform a simple school eco-club interface into an authoritative, professional, yet deeply accessible digital ecosystem. We don’t just "list" information; we "curate" it.

---

## 2. Colors & Surface Philosophy

The palette is rooted in a deep, chlorophyll green complemented by soft, loamy earth tones.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to define sections. Layout boundaries must be established exclusively through background color shifts or tonal transitions. For example, a `surface-container-low` section should sit directly on a `surface` background to create a soft, natural break.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, physical layers—fine recycled paper or frosted glass. Use the hierarchy below to create "nested" depth:
*   **Base:** `surface` (#f9f9f9) - The canvas.
*   **Low Importance:** `surface-container-low` (#f2f4f4) - Subtle grouping.
*   **High Importance:** `surface-container-high` (#e6e9e9) - Prominent content blocks.
*   **Floating/Active:** `surface-container-lowest` (#ffffff) - Cards or modals that need to "pop."

### The "Glass & Gradient" Rule
To inject "soul" into the interface, use **Glassmorphism** for floating navigation or overlay elements. Apply a 12px-20px backdrop-blur to `surface` colors at 80% opacity. 
*   **Signature Gradients:** For primary Hero sections or CTAs, use a subtle linear gradient from `primary` (#006f1d) to `primary-container` (#91f78e) at a 135-degree angle. This mimics the way light hits a leaf.

---

## 3. Typography

The typographic system pairs the architectural precision of **Plus Jakarta Sans** with the rhythmic readability of **Be Vietnam Pro**.

*   **Display (Plus Jakarta Sans):** Used for big, editorial moments. Set `display-lg` (3.5rem) with a tight letter-spacing (-0.02em) to create an authoritative, "magazine-cover" feel.
*   **Headlines (Plus Jakarta Sans):** Use `headline-md` (1.75rem) to introduce sections. These should feel bold and intentional.
*   **Titles & Body (Be Vietnam Pro):** `title-md` (1.125rem) is your workhorse for sub-headers. `body-lg` (1rem) provides a generous, friendly reading experience for students and faculty alike.
*   **Hierarchy Note:** Always maintain a high contrast between Display and Body sizes to ensure the "Editorial" look. Small, incremental jumps in font size feel "template-like"; large jumps feel "designed."

---

## 4. Elevation & Depth

We convey importance through **Tonal Layering** rather than structural shadows.

*   **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card placed on a `surface-container-low` background creates a natural lift.
*   **Ambient Shadows:** If a shadow is required (e.g., a floating action button), it must be extra-diffused. Use a 24px blur with 6% opacity, tinted with `on-surface` (#2f3334). Never use pure black shadows.
*   **The Ghost Border:** If accessibility requires a container edge, use `outline-variant` (#afb3b3) at **15% opacity**. This creates a "suggestion" of a border without breaking the organic flow.
*   **Roundedness:** Stick to the `xl` (1.5rem) or `lg` (1rem) tokens for main containers to reinforce the "friendly/eco" vibe. Use `full` (9999px) strictly for pills and buttons.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` background with `on-primary` text. Use `full` roundedness.
*   **Secondary:** `secondary-container` background. No border.
*   **Tertiary:** Text-only in `primary` color. Use for low-priority actions like "Learn More."

### Cards & Lists
*   **Mandate:** No divider lines. Separate list items using `spacing-4` (1rem) or by alternating background tones (`surface` to `surface-container-low`).
*   **The "Eco-Card":** A `surface-container-lowest` card with an `xl` corner radius. Use an asymmetrical image crop (e.g., top-left corner rounded at 4rem, others at 1.5rem) for a signature editorial look.

### Input Fields
*   **Style:** Soft, `surface-container-highest` backgrounds. 
*   **States:** On focus, transition the background to `surface-container-lowest` and add a 1px `primary` ghost border (20% opacity).

### Specialized Components
*   **Progress "Sprouts":** For tracking eco-goals, use custom progress bars with `primary` fills and a `tertiary-fixed` (#f9fbb7) track.
*   **Impact Chips:** Small `secondary-container` pills used to highlight environmental stats (e.g., "5kg Plastic Saved").

---

## 6. Do’s and Don’ts

### Do:
*   **Use Asymmetry:** Align text to the left but float images to the right with slight overlaps into the next section.
*   **Embrace White Space:** Use `spacing-20` (5rem) or `spacing-24` (6rem) between major sections to let the design breathe.
*   **Color as Signifier:** Use `tertiary` (muted olive) for archival or historical data and `primary` for active, "living" initiatives.

### Don’t:
*   **No Grid-Lock:** Do not feel forced to align every element to a rigid 12-column grid. Let elements "float" and overlap.
*   **No Hard Borders:** Never use a 100% opaque border to separate content.
*   **No Generic Icons:** Avoid thin, wiry icons. Use "Duotone" or "Solid" icons with rounded terminals to match the typography's friendliness.
*   **No Pure Greys:** Ensure all "greys" are tinted with the `secondary` earth tones to keep the palette feeling warm and organic.