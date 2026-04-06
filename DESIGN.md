# Design System Specification: The Resonant Monolith

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Resonant Monolith."** 

This system rejects the "utility-first" aesthetic of standard medical apps in favor of a high-end editorial experience. It is built on the tension between the surgical precision of high-tech hearing hardware and the soulful, resonant warmth of the Indian human experience. 

We move beyond the "template" look by utilizing **intentional asymmetry**—where technical data sits offset against large, sweeping serif typography—and **overlapping depth**, where product imagery breaks the boundaries of its containers to feel tactile and present. This is not just a tool; it is a premium lifestyle statement that honors both innovation and heritage.

---

## 2. Colors & Tonal Depth
The palette is anchored in trust (`primary`: `#021a35`) and punctuated by the energy of innovation (`secondary`: `#8f4e00` and `tertiary`: `#001e1e`).

### The "No-Line" Rule
To maintain a premium, seamless feel, **designers are prohibited from using 1px solid borders for sectioning.** Structural boundaries must be defined exclusively through:
*   **Background Color Shifts:** Transitioning from `surface` (`#fbf9f6`) to `surface-container-low` (`#f5f3f0`).
*   **Vertical White Space:** Using the spacing scale to create mental boundaries rather than physical ones.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the `surface-container` tiers to create "nested" depth:
*   **Base:** `surface` for the primary background.
*   **Sectioning:** `surface-container-low` for large content blocks.
*   **Emphasis:** `surface-container-lowest` (`#ffffff`) for cards or interactive elements that need to "pop" off a darker container.

### The Glass & Gradient Rule
For high-tech product features or floating navigation, utilize **Glassmorphism**. Apply a semi-transparent `surface-container` color with a `backdrop-filter: blur(20px)`. 
*   **CTAs:** Use subtle gradients transitioning from `primary` (`#021a35`) to `primary-container` (`#1a2f4b`) to provide a "soulful" depth that flat colors lack.

---

## 3. Typography: The Editorial Balance
We utilize a high-contrast typographic pairing to signal both authority and modern accessibility.

*   **Display & Headlines (Newsreader):** This serif choice conveys "Medical Heritage." It should be used with generous letter spacing in `display-lg` and `headline-lg` to create an expensive, editorial feel. 
*   **Body & Titles (Manrope):** This geometric sans-serif represents "High-Tech Precision." It provides maximum readability for clinical data and instructional text.

**Hierarchy Note:** Always pair a `headline-md` (Newsreader) with a `label-md` (Manrope) in `secondary` saffron to create a signature "Technical-Luxe" lockup.

---

## 4. Elevation & Depth
Depth in this system is achieved through **Tonal Layering** rather than traditional drop shadows.

*   **The Layering Principle:** To lift a card, do not reach for a shadow. Instead, place a `surface-container-lowest` object on a `surface-container-high` background. The subtle shift in hex value creates a sophisticated, natural lift.
*   **Ambient Shadows:** If a floating element (like a FAB or Modal) requires a shadow, use an extra-diffused blur (30px+) at 5% opacity. The shadow color must be a tinted version of `on-surface` (`#1b1c1a`), never a neutral grey.
*   **The "Ghost Border" Fallback:** For accessibility in input fields, use the `outline-variant` token at **20% opacity**. Never use 100% opacity borders; they break the "monolith" aesthetic.

---

## 5. Components

### Buttons
*   **Primary:** Uses a subtle gradient of `primary` to `primary-container`. Roundedness: `md` (`0.375rem`).
*   **Secondary:** No fill. Use `on-surface` text with a `Ghost Border` (20% opacity `outline-variant`).
*   **Interaction:** On hover, primary buttons should scale 2% and increase the gradient vibrance.

### Cards & Lists
*   **Constraint:** Absolute prohibition of divider lines.
*   **Execution:** Separate list items using 16px of vertical space. For complex data cards, use a `surface-container-low` background with `xl` (`0.75rem`) rounded corners.

### Inputs & Fields
*   **Style:** Minimalist "Underline" or "Soft Box" style.
*   **Focus State:** Transition the background to `primary-fixed` at 10% opacity. Avoid heavy focus rings; use a subtle 2px bottom-accent in `secondary` saffron.

### Feature: The "Resonance" Carousel
A custom component for Dhvanik: High-tech product shots on the left, overlapping with large-scale `display-md` typography on the right. The background should use a `tertiary-container` to `surface` soft radial gradient to mimic sound waves.

---

## 6. Do's and Don'ts

### Do
*   **Do** use "Newsreader" for all numbers in data visualizations to give them a premium, laboratory-scale feel.
*   **Do** leverage "India Saffron" (`secondary`) sparingly—only for primary actions or critical status indicators.
*   **Do** use emotive photography that features natural sunlight and "bokeh" (blurred backgrounds) to contrast against the sharp, clinical hardware shots.

### Don't
*   **Don't** use 100% black. Use `on-background` (`#1b1c1a`) for all text to maintain warmth.
*   **Don't** use standard "Material" shadows. They are too heavy for this sophisticated editorial style.
*   **Don't** crowd the screen. If a screen feels "full," increase the `surface` padding. This system thrives on "Breathing Room."