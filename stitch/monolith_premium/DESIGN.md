# Design System: Industrial Brutalism & Technical Elegance

## 1. Overview & Creative North Star
**The Creative North Star: "The Architectural Monolith"**

This design system moves away from the "template" feel of construction websites. Instead, it treats the browser as a physical site—a structural environment where weight, raw materials, and precision engineering take center stage. We reject the "blue-collar generic" look for a sophisticated, high-end editorial experience that mirrors the quality of specialist concreting.

The system breaks the standard grid through **Intentional Structural Asymmetry**. We utilize heavy, oversized typography that "bleeds" off the edges or overlaps image containers, simulating the way concrete forms overlap and lock together. The aesthetic is "Raw but Refined": the grit of construction meets the precision of architectural blueprints.

---

## 2. Colors & Tonal Depth
Our palette is rooted in the materials of the trade. Charcoal and concrete grey provide the foundation, while burnt orange acts as a high-visibility technical marker.

- **Primary (`#ffb59a` / `#f95e14`):** Use for tactical highlights. The "Burnt Orange" should feel like a heat-treated industrial marking—urgent and premium.
- **Surface Hierarchy:** 
    - **Background (`#131313`):** The "excavation" layer. All content rises from here.
    - **Surface-Container Tiers:** Use `surface-container-low` (#1c1b1b) for large structural blocks and `surface-container-high` (#2a2a2a) for elevated UI elements like navigation bars or floating cards.
- **The "No-Line" Rule:** We do not use 1px solid borders to separate sections. We define space through **Mass**. A change in section must be handled by shifting from `surface` to `surface-container-low`.
- **Signature Textures:** Main CTAs should not be flat. Apply a subtle linear gradient from `primary` (#ffb59a) to `primary-container` (#f95e14) at a 135-degree angle to give the orange a "metallic" or "liquid" depth.
- **The "Glass & Gradient" Rule:** For overlays (e.g., project modals), use `surface-variant` at 60% opacity with a `24px` backdrop blur. This simulates the look of architectural glass over raw stone.

---

## 3. Typography
The typography is designed to feel "cast" into the page—heavy, geometric, and immovable.

- **Display & Headlines (Space Grotesk):** This is our "Structural Steel." Headlines should be set with tight letter-spacing (-0.02em to -0.05em). Use `display-lg` (3.5rem) for hero statements to create an authoritative, "monolithic" presence.
- **Body & Labels (Inter):** Our "Precision Instrument." While the headlines are loud, the body text is quiet, legible, and highly functional.
- **Hierarchy as Identity:** Use extreme scale contrast. A `display-lg` headline paired with a `label-sm` technical spec creates a sophisticated, blueprint-like aesthetic.

---

## 4. Elevation & Depth
In this system, "Elevation" is not a shadow; it is a **Tonal Layer.**

- **The Layering Principle:** To "lift" a card, do not use a shadow. Place a `surface-container-highest` (#353535) object on top of a `surface-container-low` (#1c1b1b) background. The contrast in grey values provides the necessary separation.
- **Ambient Shadows:** Shadows are reserved only for "floating" action items (like a floating contact button). Use the `on-surface` color at 4% opacity with a `48px` blur. It should feel like a soft ambient occlusion, not a drop shadow.
- **The "Ghost Border":** If accessibility requires a stroke (e.g., in input fields), use `outline-variant` at 20% opacity. It should be barely perceptible, suggesting a boundary rather than enforcing a cage.

---

## 5. Components

### Buttons
- **Primary:** High-contrast Burnt Orange gradient. Hard corners (`rounded-sm`: 0.125rem). Typography: `label-md` in all-caps with increased letter spacing (+0.1em).
- **Secondary:** `surface-container-highest` background with a `ghost-border`. 
- **Interaction:** On hover, the primary button should "glow" subtly using a primary-colored shadow at 10% opacity.

### Cards & Lists
- **The "Mass" Rule:** Cards must never have dividers. Use `surface-container-lowest` for the card body and `surface-container-low` for the header/footer of the card to create internal hierarchy.
- **Layout:** Use generous vertical padding (`spacing-xl`) to let high-end photography breathe.

### Input Fields
- **Industrial Minimalist:** Transparent background with a `ghost-border` bottom-stroke only. When focused, the bottom-stroke transforms into the `primary` burnt orange.

### Structural Markers (Custom Component)
- **The "Datum" Line:** Use thin, vertical `primary` orange lines (2px wide) to lead the eye between sections. This mimics the survey lines used on construction sites.

---

## 6. Do's and Don'ts

### Do:
- **Do** overlap elements. Let a headline sit 20px over a photo to create architectural depth.
- **Do** use high-contrast imagery (black and white photography of concrete textures works exceptionally well with the orange accent).
- **Do** respect the grid, then break it intentionally (e.g., offset a column by 5% to create tension).

### Don't:
- **Don't** use rounded corners above `0.25rem`. This system is about hard edges and structural integrity.
- **Don't** use standard "Web Blue" for links. All interactive elements are Burnt Orange or White.
- **Don't** use drop shadows to solve legibility issues. If text isn't readable, adjust the background surface tier or add a semi-transparent overlay.