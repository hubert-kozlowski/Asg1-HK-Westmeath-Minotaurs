# CSS Guide — deep-dive (short + useful)

This file explains the non-obvious CSS patterns used in `style.css`. Read it when you want to tweak things without breaking layout.

1. CSS Variables (the easy control panel)

- Edit `:root` variables to change colors, radii, shadows and timings.
- Use them everywhere — that keeps changes small and predictable.

2. Nav buttons that swap images using variables

- Each nav button class sets `--img-default` and `--img-active`.
- `.nav-btn` uses `background-image: var(--img-default)`; hover/focus swaps to `var(--img-active)`.
- Benefit: HTML is clean (just change the class) and hover images don't need JS.
- Tip: include `aria-current="page"` on the active link so keyboard & screen reader users see current state.

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

If you want, I can extract a smaller `style-condensed.css` that drops non-essential components and keeps only the basics (layout, buttons, forms, nav).
