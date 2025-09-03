# Outpacers Design System

**Version:** 1.2.0  
**Last Updated:** September 2025

A comprehensive design system for building consistent, accessible, and beautiful user interfaces across the Outpacers brand ecosystem.

## 🎯 Overview

The Outpacers Design System provides a unified set of design tokens, components, and guidelines that ensure consistency across all digital products. Built with modern CSS practices and accessibility in mind, this system enables rapid development while maintaining brand integrity.

## 📁 File Structure

```
design-system/
├── design-tokens.json    # Design tokens and variables
├── design-system.css     # Component styles and utilities
└── README.md            # This documentation
```

## 🎨 Design Tokens

### Colors

Our color palette is built around accessibility and brand consistency:

- **Primary:** `#5524E0` - Main brand color for CTAs and key elements
- **Chartreuse:** `#CCFF04` - Accent color for highlights and special elements
- **Ink:** `#101827` - Primary text color
- **Background:** `#F9F9F9` - Main page background
- **White:** `#FFFFFF` - Pure white for cards and backgrounds
- **Header:** `#000000` - Navigation header background

### Typography

**Font Families:**
- **Sans:** Inter (Primary UI font)
- **Serif:** Lora (Headings and emphasis)
- **Mono:** IBM Plex Mono (Code and technical content)
- **Libre Baskerville:** Special italic emphasis

**Font Sizes:**
- Responsive sizing using `clamp()` for fluid typography
- Scale: xs (12px) to 6xl (60px)
- Responsive breakpoints for optimal readability

**Font Weights:**
- Normal: 400
- Medium: 500
- Semibold: 600
- Bold: 700
- Extrabold: 800

### Spacing

Consistent spacing scale based on 4px grid:
- **xs:** 4px (0.25rem)
- **sm:** 8px (0.5rem)
- **md:** 16px (1rem)
- **lg:** 24px (1.5rem)
- **xl:** 32px (2rem)
- **2xl:** 48px (3rem)
- **3xl:** 64px (4rem)

### Border Radius

- **none:** 0
- **sm:** 2px (0.125rem)
- **base:** 5.6px (0.35rem) - Default radius
- **md:** 8px (0.5rem)
- **lg:** 12px (0.75rem)
- **xl:** 16px (1rem)
- **full:** 9999px (Pill shape)

### Shadows

- **sm:** Subtle elevation
- **base:** Standard card shadow
- **md:** Medium elevation
- **lg:** Large elevation
- **xl:** Maximum elevation
- **enhanced:** Special component shadow

## 🧩 Components

### Buttons

```html
<!-- Primary Button -->
<button class="btn btn-primary">Primary Action</button>

<!-- Secondary Button -->
<button class="btn btn-secondary">Secondary Action</button>

<!-- Chartreuse Button -->
<button class="btn btn-register">Featured Action</button>
```

**Features:**
- Hover effects with subtle elevation
- Consistent border radius
- Accessible focus states
- Responsive sizing

### Cards & Containers

```html
<!-- Basic Card -->
<div class="card">Card content</div>

<!-- Token Container -->
<div class="token">Token content</div>

<!-- Header Card -->
<div class="h-card">Header card content</div>

<!-- Panel -->
<div class="panel">Panel content</div>
```

### Badges & Labels

```html
<!-- Badge -->
<span class="badge">Status</span>

<!-- Label -->
<span class="label">Description text</span>
```

### Chips

```html
<div class="chip">
  <span>Tag content</span>
</div>
```

### Logo Slots

```html
<!-- Standard Logo Slot -->
<div class="logo-slot">
  <img src="logo.png" alt="Logo" class="logo-img">
</div>

<!-- Black Background Logo Slot -->
<div class="logo-slot bg-black">
  <svg>...</svg>
</div>
```

### Special Components

#### Slab Square
```html
<span class="slab-square">
  Highlighted text
  <div class="bolt"></div>
</span>
```

#### Mixed Headlines
```html
<div class="mixed-headline">
  Regular text with <span class="italic-text">italic emphasis</span>
</div>
```

## 🛠️ Utility Classes

### Layout
- `.container` - Standard width container (1200px)
- `.container-wide` - Wide container (1400px)
- `.container-narrow` - Narrow container (800px)
- `.section` - Standard section padding
- `.section-sm` - Small section padding
- `.section-lg` - Large section padding

### Grid & Flexbox
- `.grid-auto` - Auto-fitting grid
- `.grid-2`, `.grid-3`, `.grid-4` - Fixed column grids
- `.flex`, `.flex-col`, `.flex-wrap`
- `.items-center`, `.justify-between`

### Spacing
- Margin: `.m-{size}`, `.mt-{size}`, `.mb-{size}`, `.ml-{size}`, `.mr-{size}`
- Padding: `.p-{size}`, `.pt-{size}`, `.pb-{size}`, `.pl-{size}`, `.pr-{size}`
- Combined: `.px-{size}`, `.py-{size}`

### Typography
- `.text-center`, `.text-left`, `.text-right`
- `.font-sans`, `.font-serif`, `.font-mono`, `.font-libre-baskerville`
- `.leading-tight`, `.leading-normal`, `.leading-relaxed`
- `.ink` - Primary text color
- `.text-muted` - Secondary text color

### Display & Position
- `.hidden`, `.block`, `.inline`, `.inline-block`
- `.relative`, `.absolute`, `.fixed`, `.sticky`
- `.overflow-hidden`, `.overflow-auto`

### Responsive Utilities
- `.sm:`, `.md:`, `.lg:` prefixes for responsive behavior
- Example: `.md:grid-cols-3` - 3 columns on medium screens and up

## 📱 Responsive Design

The design system is built with mobile-first responsive design:

- **Mobile:** Base styles (default)
- **Small (640px+):** `.sm:` prefixed utilities
- **Medium (768px+):** `.md:` prefixed utilities  
- **Large (1024px+):** `.lg:` prefixed utilities

## ♿ Accessibility

- WCAG AA compliant color contrast ratios
- Focus states for all interactive elements
- Screen reader friendly markup
- Keyboard navigation support
- Semantic HTML structure

## 🚀 Getting Started

### 1. Include the CSS

```html
<link rel="stylesheet" href="design-system/design-system.css">
```

### 2. Add Google Fonts

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Lora:wght@400;500;600;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
```

### 3. Use the Components

```html
<!-- Basic page structure -->
<header class="bg-[var(--header)] text-white">
  <div class="container">
    <nav class="flex items-center justify-between">
      <div class="flex items-center gap-3">
        <img src="logo.png" alt="Logo" class="h-8">
      </div>
      <div class="hidden md:flex items-center gap-6">
        <a href="#section1">Section 1</a>
        <a href="#section2">Section 2</a>
      </div>
      <button class="btn btn-primary">CTA</button>
    </nav>
  </div>
</header>

<main>
  <section class="section">
    <div class="container">
      <h1 class="text-5xl md:text-6xl font-extrabold leading-tight">
        Main Headline
      </h1>
      <p class="text-lg text-muted max-w-2xl">
        Supporting text with proper hierarchy.
      </p>
    </div>
  </section>
</main>
```

## 🎨 Customization

### CSS Variables

Override design tokens using CSS custom properties:

```css
:root {
  --primary: #your-color;
  --radius: 0.5rem;
  --font-sans: 'Your Font', sans-serif;
}
```

### Component Modifiers

Extend components with modifier classes:

```css
.btn.btn-large {
  padding: 1rem 2rem;
  font-size: 1.125rem;
}

.card.card-elevated {
  box-shadow: var(--shadow-lg);
}
```

## 🔧 Development

### Adding New Components

1. **Design Token:** Add to `design-tokens.json`
2. **CSS:** Add to `design-system.css`
3. **Documentation:** Update this README

### Component Structure

```css
/* Component Name */
.component-name {
  /* Base styles */
}

.component-name--modifier {
  /* Modifier styles */
}

.component-name__element {
  /* Element styles */
}

/* Responsive variants */
@media (min-width: 768px) {
  .md\:component-name {
    /* Medium screen styles */
  }
}
```

### Naming Conventions

- **Components:** kebab-case (`.btn-primary`)
- **Modifiers:** kebab-case (`.btn--large`)
- **Elements:** kebab-case (`.card__header`)
- **Utilities:** kebab-case (`.text-center`)

## 📚 Examples

### Navigation Bar

```html
<nav class="flex items-center justify-between p-4 bg-white border-b border-[var(--border)]">
  <div class="flex items-center gap-3">
    <img src="logo.png" alt="Logo" class="h-8">
    <span class="font-semibold text-lg">Brand Name</span>
  </div>
  
  <div class="hidden md:flex items-center gap-6">
    <a href="#home" class="hover:opacity-100 opacity-90">Home</a>
    <a href="#about" class="hover:opacity-100 opacity-90">About</a>
    <a href="#contact" class="hover:opacity-100 opacity-90">Contact</a>
  </div>
  
  <button class="btn btn-primary">Get Started</button>
</nav>
```

### Card Grid

```html
<div class="grid-auto">
  <div class="token p-4">
    <h3 class="font-semibold mb-2">Card Title</h3>
    <p class="text-muted">Card description text.</p>
  </div>
  
  <div class="token p-4">
    <h3 class="font-semibold mb-2">Another Card</h3>
    <p class="text-muted">More content here.</p>
  </div>
</div>
```

### Form Elements

```html
<form class="space-y-4">
  <div>
    <label class="label block mb-2">Email Address</label>
    <input type="email" class="w-full p-3 border border-[var(--border)] rounded-[var(--radius)]">
  </div>
  
  <button type="submit" class="btn btn-primary w-full">
    Submit Form
  </button>
</form>
```

## 🐛 Troubleshooting

### Common Issues

1. **Fonts not loading:** Check Google Fonts links
2. **CSS variables not working:** Ensure CSS file is loaded
3. **Responsive utilities not working:** Check breakpoint prefixes
4. **Component styles missing:** Verify CSS file path

### Browser Support

- **Modern browsers:** Full support
- **IE11+:** Limited support (CSS variables)
- **Mobile browsers:** Full support

## 📖 Resources

- [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

## 🤝 Contributing

1. Follow the established naming conventions
2. Ensure accessibility compliance
3. Test across different screen sizes
4. Update documentation for new components
5. Maintain backward compatibility

## 📄 License

This design system is proprietary to Outpacers and intended for internal use only.

---

**Built with ❤️ by the Outpacers Design Team**
