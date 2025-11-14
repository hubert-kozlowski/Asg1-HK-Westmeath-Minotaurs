# Westmeath Minotaurs — Site Boilerplate

A compact, purple-themed, sports-site boilerplate built around a single CSS file and simple HTML pages. This repo contains a clean layout, component styles, and a small set of pages you can reuse as a starting point for club sites, small teams, school projects, or practice sites.

Why this is useful as a boilerplate

- Single, opinionated CSS file with variables for quick theme changes.
- Mobile-first responsive design using CSS Grid and a few handy patterns (responsive video embed, gallery grid, sticky table header).
- Accessible focus states and reduced-motion support.
- Minimal JS (ideally none) — everything uses semantic HTML + CSS.

Quick start

1. Copy the repo folder for a new project.
2. Replace images in `images/` and update nav button images in `images/buttons/`.
3. Update theme colors by editing the variables at the top of `style.css` (see `THEME.md`).
4. Edit the HTML pages in `pages/` to add content. The CSS aims to work with plain semantic markup.

Files of interest

- `style.css` — main stylesheet (variables, components, responsive rules).
- `pages/` — example pages (index, about, join, game pages). Use them as templates.
- `images/` — assets & nav button images.

How to use this as a boilerplate

- Keep `:root` variables as the first place to edit colors, radii, and motion timing.
- Reuse classes like `.panel`, `.card`, `.btn`, `.surface-dark` to keep markup consistent.
- For matchups, swap theme helper classes (e.g. `.theme-minotaurs-rebels`) to change home/away coloring.

Next docs

- `CSS_GUIDE.md` — technical notes about the CSS patterns used and why they exist.
- `THEME.md` — how to change colors and add themes.
- `USAGE.md` — how to convert this repo into a new project quickly (copy, replace assets, update variables).

Accessibility & best practices

- Focus styles use `:focus-visible` to avoid keyboard focus being hidden.
- `prefers-reduced-motion` is respected for users who prefer less animation.
- Use `alt` text for images and meaningful link text.

License
Feel free to copy and reuse this for assignments and small projects. If you publish commercially, add a proper license file.

---

Small, practical docs live next to the CSS—open `CSS_GUIDE.md` and `THEME.md` for details.
