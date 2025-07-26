# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio website based on the "Massively" template by HTML5 UP. It's a pure HTML/CSS/JavaScript site with no build process or package manager required.

## Development Commands

Since this is a static site, there are no build commands. To develop locally, use any HTTP server:

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (if available)
npx http-server -p 8000

# Or simply open index.html directly in a browser
```

## Architecture

The site follows a traditional static website structure:

- **HTML Pages**: Located at root level (index.html, generic.html, elements.html)
- **Assets**: All CSS, JS, and SASS files in `/assets/`
- **Styles**: Pre-compiled CSS in `/assets/css/`, source SASS in `/assets/sass/`
- **Scripts**: jQuery-based JavaScript in `/assets/js/`
- **Images**: Site images in `/images/`

### SASS Organization
- `/assets/sass/base/`: Reset, typography, page fundamentals
- `/assets/sass/components/`: UI components (buttons, forms, tiles)
- `/assets/sass/layout/`: Layout structures (header, footer, nav, wrapper)
- `/assets/sass/libs/`: SASS utilities, mixins, and vendor includes

### JavaScript Structure
- `main.js`: Core site functionality (parallax, smooth scroll, responsive nav)
- `util.js`: Helper utilities for browser/viewport detection
- `jquery.min.js` and `jquery.scrollex.min.js`: Dependencies

## Key Files

- `index.html`: Main landing page with intro, projects, and about sections
- `generic.html`: International Scholar Program page
- `elements.html`: CV/Resume page
- `guitar.html`: Referenced in navigation but currently missing

## Deployment

This site can be deployed to any static hosting service:
- GitHub Pages: Push to repo and enable in settings
- Netlify/Vercel: Connect repo and it will auto-deploy
- Traditional hosting: Upload all files via FTP

## Important Notes

1. **No Build Process**: CSS is already compiled from SASS. Edit the compiled CSS directly or set up a SASS watcher if you need to modify styles extensively.

2. **Missing Page**: `guitar.html` is referenced in the navigation but doesn't exist. Either create this page or remove the navigation link.

3. **Template Content**: Many sections still contain placeholder content from the original template (blog posts with 2017 dates, generic descriptions).

4. **jQuery Dependency**: The site heavily relies on jQuery for interactions. Any new JavaScript should follow the existing jQuery patterns.

5. **Responsive Design**: The site uses CSS media queries for responsiveness. Test changes across different screen sizes.

## Common Tasks

### Adding a New Page
1. Copy an existing HTML file (e.g., `generic.html`) as a template
2. Update the page title and content
3. Ensure navigation links are updated in all pages

### Modifying Styles
- For quick changes: Edit `/assets/css/main.css` directly
- For extensive changes: Set up a SASS compiler and work with files in `/assets/sass/`

### Updating Navigation
- Navigation HTML is duplicated in each page
- Update the nav section in all HTML files to maintain consistency

### Working with Images
- Place images in `/images/` directory
- Background images are handled via CSS in the intro section
- Use responsive image techniques for different screen sizes