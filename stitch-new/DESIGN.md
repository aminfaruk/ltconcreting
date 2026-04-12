```markdown
# Design System Document: Tactical Warmth & Structural Elegance

## 1. Overview & Creative North Star: "The Human Architect"
This design system moves away from the cold, industrial "charcoal and steel" tropes of the construction industry. Our Creative North Star is **"The Human Architect"**—an editorial-inspired framework that balances the physical weight of construction with the airy openness of modern design. 

By leveraging intentional asymmetry, oversized typography, and layered tonal surfaces, we replace rigid "templated" grids with a bespoke, curated experience. The goal is to make the user feel like they are stepping into a sun-lit architectural studio: professional, high-end, yet fundamentally inviting.

---

## 2. Colors & Tonal Depth
We have abandoned harsh blacks and grays for a palette inspired by warm concrete, limestone, and raw earth.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning or containment. Boundaries must be defined solely through background shifts. For example, a `surface-container-low` section should sit directly against a `surface` background. The transition of tone is the divider.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of materials.
*   **Background (`#fbf9f6`):** The primary canvas.
*   **Surface Tiers:** Use `surface-container-low` (`#f5f3f0`) for large background blocks and `surface-container-highest` (`#e4e2df`) for interactive elements that need to feel "closer" to the user.
*   **The Glass & Gradient Rule:** To avoid a flat, "out-of-the-box" appearance, floating headers or navigation menus should utilize a semi-transparent `surface` color with a `20px` backdrop-blur. 
*   **Signature Textures:** For primary CTAs, do not use flat hex codes. Apply a subtle linear gradient from `primary` (#a43700) to `primary_container` (#cd4700) at a 135-degree angle to provide a "forged" depth.

---

## 3. Typography: Strong & Accessible
We pair **Plus Jakarta Sans** (Headings) with **Manrope** (Body) to create a "Technical-Chic" aesthetic.

*   **Display-LG (Plus Jakarta Sans, 3.5rem):** Use for hero statements. The slightly rounded terminals of Jakarta Sans offer a friendly, approachable strength that traditional geometric sans-serifs lack.
*   **Headline Scale:** Headlines should be set with tight letter-spacing (-0.02em) to feel authoritative.
*   **Body-LG (Manrope, 1rem):** Used for narrative descriptions. Manrope’s high x-height ensures readability even against textured backgrounds.
*   **Editorial Hierarchy:** Use `primary` (#a43700) sparingly for "Kicker" text (small labels above headlines) to draw the eye without overwhelming the page.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are a last resort. We communicate hierarchy through light and material density.

*   **The Layering Principle:** Depth is achieved by stacking. Place a `surface_container_lowest` card on a `surface_container_low` section. The minute shift in warmth creates a natural "lift."
*   **Ambient Shadows:** If a card must float (e.g., a featured project), use a shadow with a 40px blur, 0% spread, and an opacity of 5%. The color must be a tint of `on_surface` (#1b1c1a), never pure black.
*   **The "Ghost Border" Fallback:** If a container requires definition for accessibility, use the `outline_variant` token at **15% opacity**. This creates a "suggestion" of a boundary rather than a hard cage.
*   **Glassmorphism:** Use for overlays. A `surface_container` with 80% opacity and a heavy blur allows the "concrete" tones of the background to bleed through, softening the layout.

---

## 5. Components

### Buttons
*   **Primary:** A gradient of `primary` to `primary_container`. Border-radius set to `md` (0.75rem). No shadow; the color weight provides the "clickability."
*   **Secondary:** `surface_container_highest` background with `on_surface` text. This feels like an "inlaid" button, integrated into the architecture.

### Cards & Lists
*   **The Forbid Rule:** No horizontal dividers. Separate list items using `1.5rem` of vertical whitespace (Gap) or by alternating background tones between `surface_container_low` and `surface_container_lowest`.
*   **Card Shapes:** Use `xl` (1.5rem) corner radius for project cards to lean into the "inviting" aspect of the brief.

### Input Fields
*   **State:** Default state uses `surface_container_high`. On focus, transition to `surface_lowest` with a 1px `primary` ghost border (20% opacity). This mimics a light turning on within the field.

### Selection Chips
*   **Style:** Pill-shaped (`full` roundedness). Use `surface_variant` for unselected and `primary_fixed` for selected states to keep the palette warm.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical layouts. A text block on the left and an image slightly offset to the right creates an editorial, high-end feel.
*   **Do** use large amounts of "Concrete" space. Padding should be generous (use `xl` scale) to emphasize openness.
*   **Do** use `tertiary` (#005ab7) for subtle links or "Trust" markers (e.g., certifications), as blue reinforces reliability against the warm palette.

### Don’t:
*   **Don't** use pure black (#000000) for text. Always use `on_surface` (#1b1c1a) to maintain the "warm concrete" softness.
*   **Don't** use 90-degree corners for buttons or containers. The brief calls for "inviting"—always use at least `sm` (0.25rem) or `md` (0.75rem) radii.
*   **Don't** clutter. If a section feels busy, increase the background-tone shift instead of adding lines or boxes.