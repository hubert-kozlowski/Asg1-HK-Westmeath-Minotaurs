# THEME.md — tweak the purple vibe

This project uses CSS variables for theming. Most colors and subtle UI tokens live at the top of `style.css` in the `:root` block.

Primary variables to change

- `--color-primary` — main brand color (purple in this theme).
- `--accent` — used for highlights, borders and accents.
- `--bg-dark`, `--bg-card`, `--bg-dark-alt` — background surfaces (page vs cards vs stripes).
- `--text-light`, `--text-muted` — text colors.

How to quickly create a new theme

1. Add a theme class near the bottom of `style.css`, similar to the existing `.theme-*` helpers:

   .theme-new { --color-primary: #123456; --accent: #ab12ef; }

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

Want a sample color palette for a different team? Tell me the colors and I’ll auto-generate a theme block you can paste into `style.css`.
