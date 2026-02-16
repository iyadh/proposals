# Tamhees Brand Identity Proposal - AGENTS.md

## Project Overview

This is a static HTML/CSS project for presenting brand identity directions for Tamhees (تمحيص), an Islamic financial and Sharia consulting firm. The site showcases three distinct visual directions with logo variations, color palettes, and typography systems.

## Project Structure

```
/
├── index.html          # Main landing page with direction cards
├── direction-1.html    # Direction 1: Geometric Precision
├── direction-2.html    # Direction 2: Layered Transparency
├── direction-3.html    # Direction 3: The Calibrated Mark
└── .nojekyll           # Disables Jekyll processing for GitHub Pages
```

## Build/Lint/Test Commands

This is a static HTML project with no build tools, package managers, or test frameworks.

### Local Development

```bash
# Open in default browser
open index.html

# Start a simple HTTP server (Python 3)
python3 -m http.server 8000

# Start a simple HTTP server (Node.js, if available)
npx serve .

# Start a simple HTTP server (PHP, if available)
php -S localhost:8000
```

### Validation

```bash
# Validate HTML (requires html5validator)
html5validator --root .

# Check for broken links (requires linkchecker)
linkchecker http://localhost:8000
```

## Code Style Guidelines

### HTML

- Use HTML5 doctype: `<!doctype html>`
- Use lowercase for HTML tags and attributes
- Use 4-space indentation
- Self-closing tags should have a trailing slash: `<meta charset="UTF-8" />`
- Include `lang` attribute on `<html>` element: `<html lang="en">`
- Use semantic HTML elements: `<header>`, `<section>`, `<footer>`, `<nav>`
- SVG elements should be inline for optimal performance
- Comment out unused code rather than deleting if it may be needed later

### CSS

- Use CSS custom properties (variables) for colors and theming:

```css
:root {
    --color-bg: #f1f3f8;
    --color-accent: #6b9af0;
    --color-primary: #1456e1;
    --color-dark: #060d1d;
}
```

- Use 4-space indentation
- Group related styles with section comments:

```css
/* Header Section */
/* Cards Grid */
/* Typography Section */
```

- Mobile-first responsive design with media queries:

```css
@media (max-width: 1100px) {
    .directions-grid {
        grid-template-columns: 1fr;
    }
}
```

- Use modern CSS features: CSS Grid, Flexbox, CSS custom properties
- Use shorthand properties where appropriate:

```css
/* Good */
margin: 0 auto;
padding: 60px 40px;

/* Avoid verbose forms */
margin-top: 0;
margin-bottom: 0;
margin-left: auto;
margin-right: auto;
```

- Border-radius values: 4px, 8px, 12px, 16px
- Box shadows should be subtle: `0 4px 30px rgba(0, 0, 0, 0.06)`

### Typography

- Primary font stack: Google Fonts (Inter, Playfair Display, Sofia Sans Condensed, Red Hat Text, Tenor Sans, Zalando Sans Expanded, Geist)
- Headings typically use condensed/expanded sans-serif fonts with letter-spacing
- Body text uses clean sans-serif fonts with line-height: 1.6-1.8
- Letter-spacing for uppercase headings: 2px-10px

### Color Naming

Use semantic color names in CSS variables:

```css
/* Preferred - semantic naming */
--color-bg: #f1f3f8;
--color-accent: #6b9af0;
--color-primary: #1456e1;
--color-dark: #060d1d;

/* Avoid - literal naming */
--light-blue: #f1f3f8;
--medium-blue: #6b9af0;
```

### Responsive Design

- Use CSS Grid for multi-column layouts
- Breakpoints: 700px, 1100px
- Max container width: 1400px
- Use `max-width` with `margin: 0 auto` for centering

### Accessibility

- Ensure sufficient color contrast (minimum 4.5:1 for body text)
- Use meaningful alt text for images
- Maintain visual hierarchy with font sizes and weights
- Ensure interactive elements have adequate touch targets (minimum 44x44px)

### File Naming

- Use lowercase with hyphens: `direction-1.html`
- Keep file names descriptive and concise

### SVG Graphics

- Inline SVG elements for logo and icon graphics
- Use appropriate viewBox dimensions
- Use currentColor for icons that need color inheritance
- Optimize SVG paths to reduce file size

## Deployment

This project is designed for static hosting (GitHub Pages, Netlify, Vercel, etc.). The `.nojekyll` file ensures GitHub Pages processes the site correctly.

## Design System Notes

### Direction 1: Geometric Precision
- Colors: Ice Blue (#F1F3F8), Periwinkle (#6B9AF0), Royal Blue (#1456E1), Midnight (#060D1D)
- Fonts: Sofia Sans Condensed (headlines), Red Hat Text (body)

### Direction 2: Layered Transparency
- Colors: Burgundy (#4D1831), Terracotta (#724542), Cream (#F4ECD8), Deep Violet (#1A1829)
- Fonts: Tenor Sans (headlines), Inter (body)

### Direction 3: The Calibrated Mark
- Colors: Sage (#E3E8DC), Cyan (#5CD9F6), Lime (#C0F05B), Indigo (#00004D)
- Fonts: Zalando Sans Expanded (headlines), Geist (body)
