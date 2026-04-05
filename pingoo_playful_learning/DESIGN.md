# Design System Strategy: The Playful Academy

## 1. Overview & Creative North Star: "The Digital Hug"
This design system moves away from the cold, rigid structures of traditional EdTech. Our North Star is **"The Digital Hug"**—an experience that feels as safe and warm as a physical classroom but as exciting as a premium storybook. 

To achieve a "High-End Editorial" feel for a children's brand, we reject the "template" look of boxes and lines. Instead, we use **Organic Asymmetry** and **Tonal Depth**. Layouts should feel like they are floating in a soft, airy space. Elements shouldn’t just sit on a grid; they should nestle into one another using overlapping wave shapes, "bubbly" containers, and significant negative space to ensure the interface never feels cluttered for young learners or busy parents.

---

## 2. Colors: Tonal Warmth
Our palette avoids harsh contrasts in favor of a sophisticated, sun-drenched warmth.

### The "No-Line" Rule
**Borders are prohibited for sectioning.** To separate a lesson module from a navigation bar, use a background shift (e.g., a `surface-container-low` section sitting on a `surface` background). If you feel the urge to draw a line, use 32px of white space instead.

### Surface Hierarchy & Nesting
Treat the UI as a series of soft, stacked layers:
*   **Base:** `surface` (#fcf5ef) – The canvas.
*   **Sections:** `surface-container-low` (#f7f0e9) – Large structural areas.
*   **Interactive Cards:** `surface-container-lowest` (#ffffff) – To make content "pop" with a clean, high-end feel.
*   **Accents:** Use `secondary` (#005f99) for trust-based elements (Parents' area) and `primary` (#9c3f00) for action-based elements (Kids' play).

### The "Glass & Gradient" Rule
While buttons remain flat per requirements, use **Glassmorphism** for floating overlays (like progress rewards or mascot dialogues). Use a `surface` color at 80% opacity with a `20px` backdrop-blur. 
*   *Signature Texture:* Use a subtle linear gradient on large Hero backgrounds only (from `primary` to `primary-container`) to give the sky-view an editorial "glow."

---

## 3. Typography: Playful Authority
We pair the exuberant **Fredoka One** with the highly legible **Nunito** (implemented via the BeVietnamPro/PlusJakarta scales for professional weight distribution).

*   **Display (Fredoka One):** Used for "Big Moments"—level completions, welcome screens, and celebratory headers. It conveys the "Joyful" brand pillar.
*   **Body (Nunito):** Used for instructions and parent-facing fine print. The increased x-height ensures readability for early readers (ages 6-8).
*   **Hierarchy Note:** Always lead with a `display-lg` headline followed by a generous `body-lg` sub-text. Avoid "medium" sizes; go big or stay functional.

---

## 4. Elevation & Depth: Tonal Layering
We define importance through color weight, not drop shadows.

*   **The Layering Principle:** To highlight a "Pingoo Tip," place a `tertiary-container` card on top of a `surface` background. The shift from off-white to gold (#feb246) creates an instant focal point without structural clutter.
*   **Ambient Shadows:** If an element must float (e.g., a "Back to Top" button), use a shadow tinted with `primary` at 6% opacity. 
    *   *Formula:* `0px 12px 32px rgba(156, 63, 0, 0.06)`.
*   **The "Ghost Border" Fallback:** For input fields only, use `outline-variant` at 20% opacity. It should be barely visible—a "suggestion" of a boundary.

---

## 5. Components: Soft & Intentional

### Buttons (The "Bubbly" CTA)
*   **Primary:** `primary` background with `on-primary` text. **Radius: 16px.** No gradients. 
*   **Secondary:** `secondary-container` background. Feels "Safe/Trustworthy."
*   **State:** On hover, the button should scale up by 4% rather than changing color, maintaining the "Joyful" interaction.

### Cards (The "Cloud" Container)
*   **Style:** Background `surface-container-lowest` (#ffffff), **Radius: 24px.**
*   **Constraint:** No dividers. Use a `1.5rem (md)` padding to let content breathe.

### Input Fields
*   **Style:** Background `surface-container-highest`, **Radius: 12px.**
*   **Focus:** A 2px "Ghost Border" of `primary` appears only on interaction.

### Floating Mascot Dialogue (Custom Component)
*   A glassmorphic speech bubble using `surface` at 80% opacity, featuring Pingoo the Penguin partially overlapping the frame to break the "grid" and add depth.

---

## 6. Do’s and Don’ts

### Do:
*   **Use Asymmetry:** Place decorative "Soft Stars" or "Confetti" tokens partially off-screen to create a sense of infinite play.
*   **Embrace the Wave:** Use large, sweeping wave shapes to transition between white and off-white background sections.
*   **Prioritize Icons:** Use Material Rounded icons at a larger-than-standard size (28px+) to ensure they are "tappable" for tiny fingers.

### Don’t:
*   **No Sharp Corners:** Anything less than a 12px radius is a bug.
*   **No Pure Black:** Use `on-surface` (#312e2b) for text. Pure black is too harsh for the "Warm/Safe" brand intent.
*   **No Clutter:** If a screen has more than three distinct "blocks" of information, move the third block to a new page or a horizontal scroll.