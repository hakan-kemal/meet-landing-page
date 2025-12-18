# Meet Landing Page

A responsive landing page for Meet - a virtual meeting and collaboration platform. Built as part of the [Frontend Mentor](https://www.frontendmentor.io/) Building Responsive Layouts learning path.

## 🎯 Overview

This project showcases a modern landing page featuring a hero section with split images, an image gallery, and a full-width footer with background overlay. The layout adapts seamlessly across mobile, tablet, and desktop viewports using a mobile-first responsive design approach.

### Links

- Solution URL: [GitHub Repository](https://github.com/hakan-kemal/meet-landing-page)
- Live Site URL: Add your live site URL here

## 🛠 My Process

### Built With

- HTML5 - Semantic markup with ARIA labels
- CSS3 - Modern styling techniques
  - CSS Custom Properties (CSS Variables)
  - CSS Grid Layout
  - Flexbox Layout
  - Mobile-first workflow
  - CSS Nesting
- Google Fonts - [Red Hat Display](https://fonts.google.com/specimen/Red+Hat+Display)

### What I Learned

This project reinforced several key concepts:

**Advanced CSS Custom Properties**: Organized design tokens comprehensively using CSS variables for colors, typography, spacing, and other design elements:

```css
:root {
  /* Colors */
  --color-cyan-600: hsl(192, 37%, 48%);
  --color-purple-600: hsl(268, 34%, 53%);
  --color-slate-900: hsl(240, 21%, 20%);
  /* Spacing System */
  --spacing-200: 1rem;
  --spacing-400: 2rem;
  --spacing-800: 4rem;
}
```

**Responsive Background Images with Overlays**: Created a sophisticated footer with gradient overlay and responsive background images:

```css
.footer-content {
  background: linear-gradient(rgba(77, 150, 168, 0.9), rgba(77, 150, 168, 0.9)),
    url('/assets/mobile/image-footer.jpg');
  background-position: center;
  background-size: cover;
}

@media (min-width: 48rem) {
  .footer-content {
    background-image: linear-gradient(
        rgba(77, 150, 168, 0.9),
        rgba(77, 150, 168, 0.9)
      ), url('/assets/tablet/image-footer.jpg');
  }
}
```

**CSS Grid for Responsive Gallery**: Implemented a flexible grid that adapts from 2 columns on mobile to 4 columns on tablet and above:

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--spacing-200);
}

@media (min-width: 48rem) {
  .gallery {
    grid-template-columns: repeat(4, 1fr);
  }
}
```

**Conditional Image Display**: Used CSS to show/hide different hero images based on viewport size:

```css
.hero-image.desktop-only {
  display: none;
}

@media (min-width: 90rem) {
  .hero-image.desktop-only {
    display: block;
  }
  .hero-image.tablet-only {
    display: none;
  }
}
```

**Modern CSS Nesting**: Leveraged CSS nesting for cleaner, more maintainable code:

```css
.btn-primary {
  background-color: var(--color-cyan-600);

  &:hover {
    background-color: var(--color-cyan-600-hover);
  }

  & .version {
    color: var(--color-cyan-300);
  }
}
```

### Continued Development

Areas I want to focus on in future projects:

- Implementing CSS animations for button hovers and page transitions
- Exploring CSS container queries for component-level responsiveness
- Adding JavaScript for interactive features like modal dialogs
- Deepening accessibility knowledge with keyboard navigation patterns
- Optimizing images with modern formats like WebP and AVIF

### Useful Resources

- [MDN Web Docs - CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) - Comprehensive guide on CSS variables
- [CSS-Tricks - A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) - Excellent visual reference for Grid properties
- [web.dev - Responsive Images](https://web.dev/learn/design/responsive-images) - Best practices for responsive images

## 👤 Author

- Frontend Mentor - [@hakan-kemal](https://www.frontendmentor.io/profile/hakan-kemal)
- GitHub - [@hakan-kemal](https://github.com/hakan-kemal)

## 🙏 Acknowledgments

Thanks to Frontend Mentor for providing this challenge and the design specifications.
