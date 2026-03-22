# Tech Book Club - High-Fidelity Landing Page

A modern, responsive landing page built with a **Mobile-First** approach. This project serves as a technical demonstration of translating complex Figma design systems into performant, accessible, and maintainable CSS architecture.

## Project Overview

The objective was to engineer a pixel-perfect landing page that maintains a "physical notebook" aesthetic while ensuring 60fps performance and full accessibility.

### Key Technical Challenges Solved:

- **Complex Background Composition:** Layering SVG patterns over multi-stop radial gradients using `background-blend-mode`.
- **Mathematical Layouts:** Implementing a 10-column CSS Grid to achieve a specific $1.4\times$ width ratio for pricing components.
- **Fluid Typography:** Mapping variable fonts (Martian Mono & Inter) across a $rem$-based sizing scale for perfect legibility across all devices.

## Technical Stack & Architecture

### 1. CSS Architecture (CUBE Methodology)

I utilized a low-level approach to CSS, prioritizing **Composition** over heavy frameworks:

- **Custom Properties:** 100% tokenized colors, spacing, and border-radii for easy "theming" and site-wide updates.
- **Box Model Mastery:** Solved "Full-Bleed" background requirements within padded containers using viewport-relative units and negative margins to decouple background paint from content flow.
- **Hardware Acceleration:** Leveraged the GPU for `transform` and `opacity` transitions to ensure zero "jank" during user interactions.

### 2. Responsive Engineering

- **Mobile-First:** Styles are layered from the smallest screen up, optimizing the critical rendering path for mobile users.
- **Breakpoints:** Strategic overrides at `1024px` for a seamless transition from a single-column stack to a sophisticated multi-column desktop layout.

### 3. Accessibility & UX

- **Screen Reader Optimization:** Implemented `.sr-only` patterns to provide context for visually impaired users without breaking the visual design.
- **Smooth Navigation:** Engineered `scroll-margin-top` and `scroll-behavior: smooth` for logical, pleasant internal navigation.

## Development Environment

Developed on **Arch Linux** using **Neovim** and **Zsh**. This environment ensures a minimalist, high-performance workflow, allowing for deep focus on code quality and semantic structure.

## Project Structure

```text
├── assets/
│   ├── fonts/          # Variable fonts for optimized loading
│   ├── images/         # Optimized SVGs and compressed PNGs
├── reset.css           # Global browser normalization (CSS Reset)
├── styles.css          # Mobile-First core logic and Design Tokens
├── desktop.css         # Media queries and Desktop layout overrides
└── index.html          # Semantic HTML5 markup
```
