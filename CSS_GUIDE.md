# CSS Guide — Assignment Implementation Details

This document explains the technical CSS patterns implemented in `style.css` for the Web Authoring Assignment. These techniques demonstrate modern CSS capabilities and best practices covered in the course.

## 1. CSS Custom Properties (Variables)

**Assignment Requirement:** Demonstrates modern CSS organization and maintainability

- All colors, spacing, and timing values defined in `:root` for consistency
- Variables enable theme changes and reduce code duplication
- Example: `--color-primary: #2e235f;` used throughout instead of hardcoded hex values

## 2. CSS-Only Image State Management

**Assignment Requirement:** Interactive elements without JavaScript

- Navigation buttons use CSS variables to swap images on hover/focus
- Each `.nav-btn` variant sets `--img-default` and `--img-active` properties
- State changes handled purely in CSS using `:hover` and `:focus-visible` pseudo-classes
- Accessibility: `aria-current="page"` indicates active navigation state

3. Responsive YouTube embed (the padding trick)

- `.video-container` sets `padding-bottom: 56.25%` and `height: 0`.
- The iframe is absolutely positioned at `top:0;left:0;width:100%;height:100%` to match the aspect ratio.
- Why: works across widths without JS.

4. Grid patterns you should know

- `repeat(auto-fit, minmax(200px, 1fr))` for gallery grids: this makes responsive columns that never go below 200px.
- Explicit multi-column grids (e.g. `.next-session.ticker { grid-template-columns: auto auto 1fr auto; }`) allow a flexible stretch column using `1fr`.

5. Animations & reduced motion

- A single `@keyframes slideIn` is used for multiple classes; variables `--from-x` / `--from-y` change direction.
- Respect `prefers-reduced-motion: reduce` by disabling transitions/animations for those users.

6. Float / clearfix patterns

- Floats are used for wrapping images with text (`.float-left` / `.float-right`). Use `.clearfix` on the parent to contain floats.
- Modern alternative: use grid for new layouts. Floats are kept here for small, simple wrapping cases.

7. Advanced selectors and tricks

- `:is()` groups selectors that share the same rule, saving duplication.
- The general sibling selector `A ~ B` is used to style `.participation` depending on a `.status-*` class that appears earlier in the same item. It's a no-JS way to change a badge based on an adjacent element.
- `position: sticky` on table headers keeps the header visible while scrolling the standings table.

8. Image handling

- `object-fit: contain` for logos prevents distortion and keeps visuals consistent.
- Team logos are wrapped in small boxes with subtle background + border so they pop on dark rows.

9. Performance & best-practices

- Keep CSS selectors reasonably specific but not overly deep. Prefer utility classes for reuse.
- Avoid large `background-attachment: fixed` on mobile — it can be expensive; it's used for a subtle parallax, but test on phones.

10. Accessibility notes

- Always provide `:focus-visible` rules instead of `:focus` when possible (reduces focus outlines for mouse users).
- Use high contrast for text over colored backgrounds; the variables make switching easy.

## Assignment Learning Outcomes Demonstrated

- **CSS Architecture:** Organized stylesheet with logical sections and reusable components
- **Modern Selectors:** Advanced pseudo-classes, combinators, and `:is()` grouping
- **Responsive Design:** Mobile-first approach with strategic breakpoints
- **Accessibility:** WCAG-compliant focus management and motion preferences
- **Performance:** Efficient selectors and minimal HTTP requests
