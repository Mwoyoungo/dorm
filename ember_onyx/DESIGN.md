# Design System Document: The Cinematic Connection

## 1. Overview & Creative North Star
**Creative North Star: "The Midnight Editorial"**

This design system rejects the "utilitarian grid" of standard dating platforms in favor of an immersive, cinematic experience. It is designed to feel like a high-end digital gallery where humans—not profiles—are the focus. By utilizing a "True Black" foundation, we eliminate visual noise, allowing the vibrant, neon-fused Orange-Red accents to guide the user's emotional journey. 

We break the template look through **intentional depth** and **asymmetric focal points**. Instead of rigid rows, we use overlapping glass elements and varying border radii to create a layout that feels organic and premium. The goal is "Atmospheric Intimacy": a dark, focused environment that feels private, exclusive, and modern.

---

## 2. Colors & Surface Philosophy
The palette is rooted in absolute darkness to provide the highest possible contrast for photography and the primary accent gradient.

*   **Primary Accent:** A 45° Linear Gradient (`#FF6B35` to `#F04E30`). This is our "Heat" signature. Use it sparingly for primary actions and active states to maintain its impact.
*   **The "No-Line" Rule:** Standard 1px solid borders are strictly prohibited for sectioning. Definition must be achieved through background shifts. For example, a `surface-container-low` (#131313) card should sit on a `surface` (#0E0E0E) background. If a container needs more prominence, use a tonal shift, not a stroke.
*   **The Glass & Gradient Rule:** Floating elements (like the navigation bar or action buttons) must utilize Glassmorphism. Use `rgba(255, 255, 255, 0.1)` or `surface-variant` with a `10px` to `20px` backdrop blur. This ensures the UI feels like it’s floating *within* the space, rather than sitting on top of it.
*   **Signature Textures:** Apply a subtle 10% opacity version of the primary gradient as a mesh background in high-impact areas (like the "It's a Match!" screen) to provide visual soul and depth.

---

## 3. Typography
We use a dual-font approach to balance high-fashion editorial aesthetics with functional readability.

*   **Display & Headlines (Plus Jakarta Sans):** Used for big, bold statements. The wide apertures and modern geometry of Plus Jakarta Sans provide a premium, "magazine" feel. 
    *   *Headline-LG (2rem):* Use for user names and major section headers.
*   **Titles & Body (Inter):** Used for all functional data. Inter's tall x-height ensures maximum legibility against dark backgrounds.
    *   *Body-MD (0.875rem):* Our workhorse for bios and descriptions. Use `on-surface-variant` (#ADAAAA) for secondary text to reduce eye strain.
*   **Visual Hierarchy:** Establish dominance by pairing a `display-sm` headline in White (`#FFFFFF`) with a `label-md` in the primary accent color. This "High-Contrast Pairing" creates an immediate focal point.

---

## 4. Elevation & Depth
In a True Black environment, traditional shadows are invisible. We define depth through **Tonal Layering** and **Luminescence**.

*   **The Layering Principle:** 
    *   **Level 0 (Base):** `surface` (#0E0E0E).
    *   **Level 1 (Sections):** `surface-container-low` (#131313).
    *   **Level 2 (Cards/Interests):** `surface-container-highest` (#262626).
*   **Ambient Shadows:** For floating elements, use a "Glow Shadow" rather than a dark one. Use the primary accent color at 4%-8% opacity with a large blur (20px+) to create a soft, neon-like aura.
*   **The "Ghost Border" Fallback:** Where separation is critical (e.g., input fields), use a `1px` border using `outline-variant` (#484847) at **20% opacity**. It should be felt, not seen.
*   **Glassmorphism:** The floating bottom nav uses `rgba(26, 26, 26, 0.8)` with a `10px` backdrop blur and a `40px` (Full) border radius. This "frosted" look allows profile photos to bleed through subtly, maintaining the cinematic immersion.

---

## 5. Components

### Buttons & Actions
*   **Primary CTA:** Orange-Red 45° Gradient. No border. Text: White. Shape: `xl` radius (3rem).
*   **Secondary Action:** Glassmorphism (`rgba(255, 255, 255, 0.2)`) with `5px` backdrop blur. Shape: `md` radius (1.5rem).
*   **Active States:** Circular indicators must use the primary gradient with a neon-like glow: `box-shadow: 0 4px 15px rgba(240, 78, 48, 0.4)`.

### Cards & Discovery
*   **User Cards:** `20px` border radius. Use a `bottom-aligned` black-to-transparent gradient overlay (60% height) to ensure white typography is legible over user photos. 
*   **Interests/Pills:** Background: `#1A1A1A`. Border: `1px solid #333333`. Radius: `20px`. These are the only components allowed a visible border to mimic "stamped" physical tags.

### Inputs & Selection
*   **Input Fields:** Use `surface-container-highest` background. No bottom line. Use `md` (1.5rem) radius.
*   **Lists:** Forbid divider lines. Use `1.4rem` (Spacing 4) vertical whitespace to separate message threads. Use a `surface-bright` (#2C2C2C) background shift on press/hover.

### Custom Component: The "Vibe" Stack
An asymmetric layout for user "Interests" where pills are not perfectly aligned but slightly staggered, breaking the "grid" and feeling more like a natural collection of thoughts.

---

## 6. Do's and Don'ts

### Do
*   **DO** use whitespace as a separator. If you think you need a line, add `1rem` of space instead.
*   **DO** use high-quality imagery. The "True Black" theme is unforgiving to low-resolution photos.
*   **DO** experiment with asymmetry. Let a user's name overlap the edge of a container to create depth.

### Don't
*   **DON'T** use pure `#000000` for cards. It creates a "black hole" effect. Stick to the `surface-container` tiers.
*   **DON'T** use high-contrast white borders. They break the cinematic "Midnight" atmosphere.
*   **DON'T** clutter the UI. If a feature isn't essential to the "Connection," hide it in a glass-layered sheet.
*   **DON'T** use standard shadows. If it doesn't glow or layer tonally, it shouldn't be there.