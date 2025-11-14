# Setup & Development Guide — Assignment ASG1-HK

## Assignment Submission Checklist

**For Web Authoring Course Evaluation:**

✅ **Semantic HTML5:** All pages use proper structure (header, nav, main, section, article)  
✅ **CSS Architecture:** Single stylesheet with variables, components, responsive design  
✅ **Accessibility:** WCAG focus states, reduced motion, keyboard navigation  
✅ **Responsive Design:** Mobile-first breakpoints at 700px, 800px, 1000px, 1200px  
✅ **Modern CSS:** Custom properties, Grid, Flexbox, advanced selectors  
✅ **Performance:** Optimized images, minimal HTTP requests, efficient CSS

## Development Testing Process

**Responsive Testing:**

1. Test all breakpoints using browser DevTools device emulation
2. Verify navigation collapses appropriately on mobile
3. Check image scaling and text readability across screen sizes

**Accessibility Validation:**

1. Tab through all interactive elements (keyboard navigation test)
2. Verify focus indicators are visible and consistent
3. Test with `prefers-reduced-motion: reduce` enabled
4. Validate color contrast using WebAIM or similar tools
5. Check all images have meaningful `alt` attributes

**Cross-Browser Compatibility:**

- Chrome, Firefox, Safari, Edge (modern versions)
- Mobile Safari and Chrome (iOS/Android)

## Open Source Usage (Optional)

While this is a course assignment, the code can be referenced or adapted:

**For Learning/Practice:**

1. Fork or download the repository
2. Modify colors in `:root` variables to create new themes
3. Replace content while keeping semantic HTML structure
4. Use components (`.panel`, `.card`, `.btn`) for consistent styling

**Attribution:** If using substantial portions for other projects, please credit the original assignment.
