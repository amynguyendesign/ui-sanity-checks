---
name: ui-sanity-checks
description: Contrast, typography, spacing, and interaction rules every UI should meet. Grounded in WCAG 2.2 and industry best practices.
---

# UI Sanity Checks

Your fonts, colors, layout, and personality are yours. These checks make sure real people can actually use what you build — and that it doesn't look like nobody checked.

## Rules

### Contrast & Color
- Text contrast ≥ 4.5:1 for normal text, ≥ 3:1 for large text (≥ 18px bold or ≥ 24px) [WCAG 1.4.3]
- UI component contrast ≥ 3:1 against adjacent colors [WCAG 1.4.11]
- Never use color alone to convey meaning — always pair with text, icon, or pattern [WCAG 1.4.1]
- Avoid pure `#000` on `#FFF` for body text — prefer softened values like `#1a1a1a` on `#ffffff` to reduce eye strain [best practice]

### Typography
- Body text ≥ 16px for readable content [best practice — browser default]
- Line height ≥ 1.5× the font size [WCAG 1.4.12]
- Line width ~60–80 characters max for readability [best practice — Bringhurst]
- Headings follow sequential hierarchy: h1 → h2 → h3, never skip levels [WCAG 1.3.1]
- Use `rem` or `em` for font sizes so user browser settings are respected [best practice]
- Handle text overflow: long strings must wrap or truncate gracefully — never break layout [best practice]

### Spacing & Targets
- Clickable/tappable targets ≥ 44×44px [WCAG 2.5.5 enhanced; Apple/Google/Microsoft HIG]
- ≥ 8px gap between adjacent interactive elements [best practice]
- All spacing follows a consistent scale (e.g. 4px/8px grid) — including padding between similar components [best practice]
- Layout must work at 200% zoom with no horizontal scrolling [WCAG 1.4.4]
- Use a single consistent border-radius scale across all components [best practice]

### Interactive Elements
- Visible focus indicator on all interactive elements — ≥ 2px, contrast ≥ 3:1 [WCAG 2.4.13]
- All functionality reachable via keyboard [WCAG 2.1.1]
- Hover and focus states must be visually distinct from default state [best practice]
- Tab order follows logical reading order [WCAG 2.4.3]
- Clickable elements must use `cursor: pointer` [best practice]
- Disabled elements must look visually distinct (e.g. reduced opacity) and prevent interaction [best practice]

### Structure & Semantics
- Use semantic HTML elements: `<button>`, `<nav>`, `<main>`, `<header>`, `<section>`, `<article>` [WCAG 4.1.2]
- Every `<img>` has descriptive `alt` text (or `alt=""` if purely decorative) [WCAG 1.1.1]
- Icon-only buttons must have `aria-label` [WCAG 4.1.2]
- Form inputs must have associated `<label>` elements [WCAG 1.3.1]

### Images & Media
- Images in fixed-size containers must use `object-fit` to prevent stretching or squishing [best practice]
- Icons must be consistently sized and optically aligned with adjacent text [best practice]
- Reserve space for images and async content to prevent layout shift [best practice — CLS/Core Web Vitals]
- Custom fonts must not block rendering — ensure text remains visible during load [best practice]

### Motion & Animation
- Respect `prefers-reduced-motion` — wrap animations in the media query [WCAG 2.3.3]
- No content flashes more than 3 times per second [WCAG 2.3.1]
- Transitions ≤ 300ms for UI feedback [best practice — Nielsen Norman Group]
- Animations should be additive, never required to understand content [best practice]

## How to apply

**When generating new UI:** Follow every rule by default. No exceptions.

**When reviewing existing UI:** Audit against each rule. Flag every violation with the specific rule and source, then fix it.
