# Color System & Theming — Assignment Documentation

## Theme Architecture for Web Authoring Assignment

The Westmeath Minotaurs site uses a CSS custom properties-based theming system that demonstrates modern CSS organization and maintainability principles covered in the course.

## Core Color Variables

The entire color scheme is controlled through CSS custom properties in the `:root` selector:

- `--color-primary: #2e235f` — Minotaurs team purple (headers, navigation)
- `--accent: #7b3fb8` — Highlight color (links, focus states, call-to-actions)
- `--bg-dark: #14102b` — Main page background
- `--bg-card: #1c1333` — Card/panel surfaces
- `--bg-dark-alt: #191030` — Alternating row backgrounds (zebra stripes)
- `--text-light: #f4f4f8` — Primary text on dark backgrounds
- `--text-muted: #b5afc7` — Secondary text, less emphasis

## Assignment Design Decisions

**Purple Theme Choice:** Selected to demonstrate brand consistency across a sports website while maintaining good contrast ratios for accessibility compliance.

**Variable-Based System:** Enables easy theme modifications and demonstrates CSS custom properties usage — a modern web development standard.

## Multi-Team Theme Support

The CSS includes theme helper classes for different matchups:

2. Wrap the region you want themed in an element with that class (e.g., `<main class="theme-new">`), or apply at `body` to change the whole site.

Runtime theme switching (no JS required, basic) — recommended approach

- Keep theme variables scoped under classes (e.g., `.theme-dark`, `.theme-light`).
- Toggle the class on `body` using a tiny script or server-side logic.

Accessibility & contrast tips

- Run your chosen `--color-primary` and `--accent` through a contrast checker against `--text-light` and `--text-muted`.
- If you decide to allow light backgrounds, make sure dark text variables are set appropriately.

Small gotchas

- Some components expect dark backgrounds (shadows, filters). If you flip to a light theme, double-check shadows and border colors.
- `background-attachment: fixed` may behave oddly on mobile browsers; keep an eye on that with new themes.

## Course Learning Outcomes Demonstrated

- **CSS Custom Properties:** Modern variable usage for maintainable stylesheets
- **Color Theory:** Complementary color selection and brand consistency
- **Accessibility:** WCAG-compliant contrast ratios and usability
- **Responsive Design:** Color schemes that work across device contexts
