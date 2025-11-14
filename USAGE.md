# USAGE.md — turning this into a new project

Quick checklist to copy this repo into a new site or assignment:

1. Copy the folder into a new project directory.
2. Replace images in `images/` (team logos, buttons, gallery) with your assets.
3. Update `style.css` at the top `:root` variables for colors and radii.
4. Open `pages/index.html` and `pages/about.html` and replace content. Keep semantic tags (header, main, section, article) for best results.
5. For the nav: update the `nav-btn` classes and ensure the active link has `aria-current="page"`.
6. Test responsiveness: use browser devtools to check common breakpoints (700px, 800px, 1000px).
7. Accessibility checklist:
   - All interactive elements focusable and have visible focus (keyboard test: Tab through the page).
   - `alt` attributes on images.
   - Check color contrast for text on backgrounds.
   - Test `prefers-reduced-motion` by toggling in system settings or using the browser.

Optional: create a condensed CSS

- If you want a smaller file: remove components you don't use (matchup, standings table, gallery) and keep variables + base + buttons + forms.
- I can produce a `style-condensed.css` strip-down for you if you want.

Deployment tips

- It's a static site — upload as-is to GitHub Pages, Netlify, or any static host.
- If you deploy on GitHub Pages, set the repository homepage to the `pages` folder or adjust links accordingly.

If you want, I can also:

- Generate a `style-condensed.css` that trims unused sections so the file is much smaller.
- Make a `boilerplate.zip` with only the essentials (index, style, images placeholders, and README).

---

Tell me which of those extras you want and I'll make them.
