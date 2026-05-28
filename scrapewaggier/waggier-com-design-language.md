# Design Language: Waggier™ PaceBowl

> Extracted from `https://waggier.com/products/waggier-pacebowl-2` on April 26, 2026
> 1663 elements analyzed

This document describes the complete design language of the website. It is structured for AI/LLM consumption — use it to faithfully recreate the visual design in any framework.

## Color Palette

### Primary Colors

| Role | Hex | RGB | HSL | Usage Count |
|------|-----|-----|-----|-------------|
| Primary | `#339b43` | rgb(51, 155, 67) | hsl(129, 50%, 40%) | 86 |
| Secondary | `#ffcc00` | rgb(255, 204, 0) | hsl(48, 100%, 50%) | 112 |
| Accent | `#2d5f3f` | rgb(45, 95, 63) | hsl(142, 36%, 27%) | 1 |

### Neutral Colors

| Hex | HSL | Usage Count |
|-----|-----|-------------|
| `#121212` | hsl(0, 0%, 7%) | 2200 |
| `#ffffff` | hsl(0, 0%, 100%) | 455 |
| `#000000` | hsl(0, 0%, 0%) | 420 |
| `#ececec` | hsl(0, 0%, 93%) | 47 |
| `#2e2a39` | hsl(256, 15%, 19%) | 20 |
| `#666666` | hsl(0, 0%, 40%) | 12 |
| `#b7b7b7` | hsl(0, 0%, 72%) | 2 |
| `#e3e3e3` | hsl(0, 0%, 89%) | 1 |
| `#707070` | hsl(0, 0%, 44%) | 1 |

### Background Colors

Used on large-area elements: `#ffffff`, `#339b43`, `#e8f5e9`, `#000000`

### Text Colors

Text color palette: `#000000`, `#121212`, `#ffffff`, `#17648f`, `#339b43`, `#ececec`, `#ffcc00`, `#5433eb`, `#ffd700`, `#2e2a39`

### Gradients

```css
background-image: linear-gradient(rgba(18, 18, 18, 0.04), rgba(18, 18, 18, 0.04));
```

```css
background-image: linear-gradient(135deg, rgb(51, 155, 67) 0%, rgb(112, 185, 123) 100%);
```

### Full Color Inventory

| Hex | Contexts | Count |
|-----|----------|-------|
| `#121212` | text, border, background | 2200 |
| `#ffffff` | background, text, border | 455 |
| `#000000` | text, border, background | 420 |
| `#ffcc00` | text, border | 112 |
| `#339b43` | background, text, border | 86 |
| `#ececec` | text, border, background | 47 |
| `#17648f` | text, border | 30 |
| `#5433eb` | text, border | 26 |
| `#2e2a39` | text, border | 20 |
| `#666666` | text, border | 12 |
| `#b7b7b7` | border | 2 |
| `#2d5f3f` | background | 1 |
| `#e3e3e3` | border | 1 |
| `#707070` | background | 1 |

## Typography

### Font Families

- **Montserrat** — used for all (1309 elements)
- **Times New Roman** — used for body (195 elements)
- **Arial** — used for body (94 elements)
- **ui-sans-serif** — used for body (39 elements)
- **Material Symbols Outlined** — used for body (13 elements)
- **Nunito** — used for body (10 elements)
- **GTStandard-M** — used for body (3 elements)

### Type Scale

| Size (px) | Size (rem) | Weight | Line Height | Letter Spacing | Used On |
|-----------|------------|--------|-------------|----------------|---------|
| 50px | 3.125rem | 400 | 90px | 0.96px | div, svg, path |
| 39px | 2.4375rem | 600 | 48px | 0.78px | h2, strong |
| 31.2px | 1.95rem | 600 | 38.4px | 0.78px | h2 |
| 30px | 1.875rem | 400 | normal | normal | button, svg, path, div |
| 25px | 1.5625rem | 700 | 37.5px | 1.3px | span |
| 23.4px | 1.4625rem | 600 | 28.8px | 0.78px | h3, p, span, h2 |
| 23px | 1.4375rem | 400 | 25.3px | 0.96px | p, span, strong |
| 22.5px | 1.4063rem | 600 | 29.25px | 0.78px | h3, div, span |
| 22px | 1.375rem | 400 | 26.4px | 0.96px | p |
| 20.7px | 1.2937rem | 700 | 22.77px | 0.96px | span |
| 20px | 1.25rem | 400 | 30px | 1.3px | div, span |
| 19px | 1.1875rem | 700 | 22.8px | 1px | button, div, svg, circle |
| 18.85px | 1.1781rem | 600 | 26.1px | 0.78px | h3 |
| 18.4px | 1.15rem | 400 | 33.12px | 0.96px | div, svg, path, span |
| 18px | 1.125rem | 400 | 23.4px | 0.96px | a, p, button, span |

### Heading Scale

```css
h2 { font-size: 39px; font-weight: 600; line-height: 48px; }
h2 { font-size: 31.2px; font-weight: 600; line-height: 38.4px; }
h3 { font-size: 23.4px; font-weight: 600; line-height: 28.8px; }
h3 { font-size: 22.5px; font-weight: 600; line-height: 29.25px; }
h3 { font-size: 18.85px; font-weight: 600; line-height: 26.1px; }
h2 { font-size: 15.6px; font-weight: 600; line-height: 19.2px; }
h2 { font-size: 13px; font-weight: 400; line-height: 19.5px; }
```

### Body Text

```css
body { font-size: 16px; font-weight: 400; line-height: 28.8px; }
```

### Font Weights in Use

`400` (1561x), `600` (48x), `700` (46x), `300` (6x), `450` (1x), `500` (1x)

## Spacing

**Base unit:** 2px

| Token | Value | Rem |
|-------|-------|-----|
| spacing-1 | 1px | 0.0625rem |
| spacing-24 | 24px | 1.5rem |
| spacing-28 | 28px | 1.75rem |
| spacing-35 | 35px | 2.1875rem |
| spacing-40 | 40px | 2.5rem |
| spacing-45 | 45px | 2.8125rem |
| spacing-50 | 50px | 3.125rem |
| spacing-55 | 55px | 3.4375rem |
| spacing-60 | 60px | 3.75rem |
| spacing-68 | 68px | 4.25rem |
| spacing-90 | 90px | 5.625rem |
| spacing-98 | 98px | 6.125rem |
| spacing-110 | 110px | 6.875rem |
| spacing-200 | 200px | 12.5rem |
| spacing-273 | 273px | 17.0625rem |
| spacing-367 | 367px | 22.9375rem |
| spacing-370 | 370px | 23.125rem |

## Border Radii

| Label | Value | Count |
|-------|-------|-------|
| sm | 5px | 5 |
| md | 8px | 2 |
| lg | 12px | 36 |
| xl | 20px | 1 |
| xl | 24px | 9 |
| full | 28px | 2 |
| full | 40px | 3 |
| full | 50px | 24 |
| full | 58px | 2 |
| full | 999px | 2 |

## Box Shadows

**sm** — blur: 0px
```css
box-shadow: rgba(51, 155, 67, 0) 0px 0px 0px 2px;
```

**sm** — blur: 0px
```css
box-shadow: rgb(18, 18, 18) 0px 0px 0px 1px;
```

**sm** — blur: 3px
```css
box-shadow: rgba(0, 0, 0, 0.2) 0px 3px 3px 0px;
```

**sm** — blur: 6px
```css
box-shadow: rgba(40, 80, 150, 0.06) 0px 1px 6px 0px;
```

**xl** — blur: 20px
```css
box-shadow: rgba(18, 18, 18, 0.1) 10px 12px 20px 0px;
```

## CSS Custom Properties

### Colors

```css
--color-base-text: 18, 18, 18;
--color-shadow: 18, 18, 18;
--color-base-background-1: 255, 255, 255;
--color-base-background-2: 232, 245, 233;
--color-base-solid-button-labels: 255, 255, 255;
--color-base-outline-button-labels: 23, 100, 143;
--color-base-accent-1: 51, 155, 67;
--color-base-accent-2: 51, 155, 67;
--payment-terms-background-color: #ffffff;
--gradient-base-accent-1: #339b43;
--gradient-base-accent-2: linear-gradient(54deg, rgba(109, 56, 139, 1) 14%, rgba(105, 14, 14, 1) 85%);
--media-border-opacity: 0.1;
--media-border-width: 0px;
--product-card-image-padding: 0.0rem;
--product-card-corner-radius: 1.2rem;
--product-card-text-alignment: center;
--product-card-border-width: 0.0rem;
--product-card-border-opacity: 0.1;
--product-card-shadow-opacity: 0.1;
--product-card-shadow-visible: 1;
--product-card-shadow-horizontal-offset: 0.2rem;
--product-card-shadow-vertical-offset: 0.6rem;
--product-card-shadow-blur-radius: 1.5rem;
--collection-card-image-padding: 0.0rem;
--collection-card-corner-radius: 1.2rem;
--collection-card-text-alignment: center;
--collection-card-border-width: 0.0rem;
--collection-card-border-opacity: 0.1;
--collection-card-shadow-opacity: 0.05;
--collection-card-shadow-visible: 1;
--collection-card-shadow-horizontal-offset: 0.2rem;
--collection-card-shadow-vertical-offset: 0.6rem;
--collection-card-shadow-blur-radius: 1.5rem;
--blog-card-image-padding: 0.0rem;
--blog-card-corner-radius: 1.2rem;
--blog-card-text-alignment: center;
--blog-card-border-width: 0.0rem;
--blog-card-border-opacity: 0.1;
--blog-card-shadow-opacity: 0.05;
--blog-card-shadow-visible: 1;
--blog-card-shadow-horizontal-offset: 1.0rem;
--blog-card-shadow-vertical-offset: 1.0rem;
--blog-card-shadow-blur-radius: 3.5rem;
--slider-arrow-border-radius: 50.0%;
--popup-border-width: 1px;
--popup-border-opacity: 0.1;
--drawer-border-width: 1px;
--drawer-border-opacity: 0.1;
--text-boxes-border-opacity: 0.1;
--text-boxes-border-width: 0px;
--buttons-border-width: 2px;
--buttons-border-opacity: 1.0;
--buttons-border-offset: 0.3px;
--swatches-border-opacity: 0.0;
--swatches-selected-border-opacity: 0.5;
--pickers-border-width: 1px;
--pickers-border-color: var(--color-base-accent-1);
--pickers-border-opacity: 0.2;
--pickers-hover-border-opacity: 0.55;
--quantity-border-width: 1px;
--quantity-border-color: var(--color-base-accent-1);
--quantity-border-opacity: 0.2;
--quantity-hover-border-opacity: 0.15;
--inputs-border-width: 1px;
--inputs-border-opacity: 0.6;
--inputs-hover-border-opacity: 1;
--variant-pills-border-width: 1px;
--variant-pills-border-opacity: 0.55;
--color-card-hover: 18, 18, 18;
--accent-color: 51, 155, 67;
--color-background: 255, 255, 255;
--color-badge-background: 255, 255, 255;
--color-button-text: 255, 255, 255;
--color-button: 51, 155, 67;
--alpha-button-border: 1;
--color-icon: rgb(18, 18, 18);
--border-color: 18, 18, 18;
--color-foreground: 18, 18, 18;
--alpha-badge-border: .1;
--color-link: 23, 100, 143;
--color-badge-border: 18, 18, 18;
```

### Spacing

```css
--font-heading-letter-spacing: 0.06rem;
--media-padding: px;
--page-width-margin: 0rem;
--slider-arrow-size: 3.0rem;
--slider-arrow-icon-size: 0.6em;
--pagination-dot-spacing: 12px;
--spacing-sections-desktop: 0px;
--spacing-sections-mobile: 0px;
--grid-desktop-vertical-spacing: 40px;
--grid-desktop-horizontal-spacing: 40px;
--grid-mobile-vertical-spacing: 20px;
--grid-mobile-horizontal-spacing: 20px;
--pickers-margin-offset: 0px;
--quantity-margin-offset: 0px;
--inputs-margin-offset: 0px;
--variant-pills-text-size: 1.4rem;
--variant-pills-padding-y: 1.0rem;
--variant-pills-padding-x: 2.0rem;
```

### Typography

```css
--font-body-family: Montserrat, sans-serif;
--font-body-style: normal;
--font-body-weight: 400;
--font-body-weight-bold: 700;
--font-heading-family: Montserrat, sans-serif;
--font-heading-style: normal;
--font-heading-weight: 600;
--font-body-scale: 1.0;
--font-heading-scale: 1.3;
--font-heading-line-height: 0.3;
--text-boxes-radius: 24px;
--text-boxes-shadow-opacity: 0.0;
--text-boxes-shadow-visible: 0;
--text-boxes-shadow-horizontal-offset: 10px;
--text-boxes-shadow-vertical-offset: 12px;
--text-boxes-shadow-blur-radius: 20px;
```

### Shadows

```css
--media-shadow-opacity: 0.0;
--media-shadow-horizontal-offset: 0px;
--media-shadow-vertical-offset: 0px;
--media-shadow-blur-radius: 20px;
--media-shadow-visible: 0;
--popup-shadow-opacity: 0.1;
--popup-shadow-horizontal-offset: 10px;
--popup-shadow-vertical-offset: 12px;
--popup-shadow-blur-radius: 20px;
--drawer-shadow-opacity: 0.0;
--drawer-shadow-horizontal-offset: 0px;
--drawer-shadow-vertical-offset: 4px;
--drawer-shadow-blur-radius: 5px;
--buttons-shadow-opacity: 0.0;
--buttons-shadow-visible: 0;
--buttons-shadow-horizontal-offset: 0px;
--buttons-shadow-vertical-offset: 4px;
--buttons-shadow-blur-radius: 5px;
--pickers-shadow-opacity: 0.0;
--pickers-shadow-horizontal-offset: 0px;
--pickers-shadow-vertical-offset: 0px;
--pickers-shadow-blur-radius: 0px;
--quantity-shadow-opacity: 0.0;
--quantity-shadow-horizontal-offset: 0px;
--quantity-shadow-vertical-offset: 0px;
--quantity-shadow-blur-radius: 0px;
--inputs-shadow-opacity: 0.0;
--inputs-shadow-horizontal-offset: 0px;
--inputs-shadow-vertical-offset: 4px;
--inputs-shadow-blur-radius: 5px;
--variant-pills-shadow-opacity: 0.0;
--variant-pills-shadow-horizontal-offset: 0px;
--variant-pills-shadow-vertical-offset: 4px;
--variant-pills-shadow-blur-radius: 5px;
```

### Radii

```css
--media-radius: 12px;
--badge-corner-radius: 0.6rem;
--pagination-dot-radius: 5px;
--popup-corner-radius: 14px;
--buttons-radius: 40px;
--buttons-radius-outset: 42px;
--swatches-radius: 0.0%;
--pickers-radius: 8px;
--pickers-small-radius: 3.2px;
--pickers-radius-outset: 9px;
--quantity-radius: 8px;
--quantity-small-radius: 3.2px;
--quantity-radius-outset: 9px;
--inputs-radius: 6px;
--inputs-radius-outset: 7px;
--variant-pills-radius: 40px;
```

### Other

```css
--gradient-base-background-1: #ffffff;
--gradient-base-background-2: #e8f5e9;
--page-width: 140rem;
--pagination-dot-width: 6px;
--pagination-dot-height: 6px;
--pagination-dot-active-scale: 1.5;
--pickers-overlay-opacity: 0.08;
--pickers-hover-overlay-opacity: 0.1;
--quantity-overlay-opacity: 0.06;
--quantity-hover-overlay-opacity: 0.06;
--variant-pills-inactive-overlay-opacity: 0.0;
--duration-short: .1s;
--duration-default: .2s;
--duration-long: .5s;
--header-height: 90px;
--alpha-link: .85;
--alpha-button-background: 1;
--gradient-background: #ffffff;
```

### Dependencies

```css
--pickers-border-color: --color-base-accent-1;
--quantity-border-color: --color-base-accent-1;
```

### Semantic

```css
success: [object Object];
warning: [object Object];
error: [object Object];
info: [object Object];
```

## Breakpoints

| Name | Value | Type |
|------|-------|------|
| 400px | 400px | min-width |
| 401px | 401px | min-width |
| sm | 500px | max-width |
| md | 749px | max-width |
| md | 750px | min-width |
| md | 800px | max-width |
| 899px | 899px | max-width |
| 900px | 900px | min-width |
| lg | 989px | max-width |
| lg | 990px | min-width |
| lg | 999px | max-width |
| lg | 1000px | min-width |
| 1200px | 1200px | min-width |
| xl | 1250px | max-width |
| 1400px | 1400px | min-width |

## Transitions & Animations

**Easing functions:** `[object Object]`, `[object Object]`, `[object Object]`, `[object Object]`

**Durations:** `0.4s`, `0.15s`, `0.1s`, `0.2s`, `0.65s`, `0.3s`, `0.45s`, `0.6s`, `0.75s`, `0.9s`, `1.05s`, `1.2s`, `1.35s`, `1.5s`

### Common Transitions

```css
transition: all;
transition: color 0.4s;
transition: top 0.15s ease-out;
transition: transform 0.15s, opacity 0.15s;
transition: opacity 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
transition: box-shadow 0.1s;
transition: top 0.1s, font-size 0.1s;
transition: visibility 0.2s, background-color 0.2s;
transition: transform 0.2s;
transition: text-decoration-thickness 0.1s;
```

### Keyframe Animations

**shopify-rotator**
```css
@keyframes shopify-rotator {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(270deg); }
}
```

**shopify-dash**
```css
@keyframes shopify-dash {
  0% { stroke-dashoffset: 280; }
  50% { stroke-dashoffset: 75; transform: rotate(135deg); }
  100% { stroke-dashoffset: 280; transform: rotate(450deg); }
}
```

**acceleratedCheckoutLoadingSkeleton**
```css
@keyframes acceleratedCheckoutLoadingSkeleton {
  50% { opacity: var(--shopify-accelerated-checkout-skeleton-animation-opacity-start, 1); }
  75% { opacity: var(--shopify-accelerated-checkout-skeleton-animation-opacity-end, .5); }
  100% { opacity: var(--shopify-accelerated-checkout-skeleton-animation-opacity-start, 1); }
}
```

**ripple**
```css
@keyframes ripple {
  0% { opacity: 0; transform: none; }
  20%, 70% { opacity: 1; }
  100% { opacity: 0; transform: scale(1.5); }
}
```

**animateMenuOpen**
```css
@keyframes animateMenuOpen {
  0% { opacity: 0; transform: translateY(-1.5rem); }
  100% { opacity: 1; transform: translateY(0px); }
}
```

**spin**
```css
@keyframes spin {
  0% { transform: translate(-50%, -50%) rotate(0deg); }
  100% { transform: translate(-50%, -50%) rotate(360deg); }
}
```

**splide-loading**
```css
@keyframes splide-loading {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(1turn); }
}
```

**rotator**
```css
@keyframes rotator {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(270deg); }
}
```

**dash**
```css
@keyframes dash {
  0% { stroke-dashoffset: 280; }
  50% { stroke-dashoffset: 75; transform: rotate(135deg); }
  100% { stroke-dashoffset: 280; transform: rotate(450deg); }
}
```

**slideBar**
```css
@keyframes slideBar {
  0% { background-position-x: 0px; }
  100% { background-position-x: 10rem; }
}
```

## Component Patterns

Detected UI component patterns and their most common styles:

### Buttons (51 instances)

```css
.button {
  background-color: rgb(255, 255, 255);
  color: rgb(18, 18, 18);
  font-size: 13.3333px;
  font-weight: 400;
  padding-top: 0px;
  padding-right: 0px;
  border-radius: 0px;
}
```

### Cards (29 instances)

```css
.card {
  background-color: rgb(255, 255, 255);
  border-radius: 0px;
  box-shadow: rgba(18, 18, 18, 0.1) 10px 12px 20px 0px;
  padding-top: 0px;
  padding-right: 0px;
}
```

### Inputs (21 instances)

```css
.input {
  background-color: rgb(255, 255, 255);
  color: rgb(0, 0, 0);
  border-color: rgb(0, 0, 0);
  border-radius: 0px;
  font-size: 13.3333px;
  padding-top: 0px;
  padding-right: 0px;
}
```

### Links (36 instances)

```css
.link {
  color: rgba(18, 18, 18, 0.9);
  font-size: 14px;
  font-weight: 400;
}
```

### Navigation (23 instances)

```css
.navigatio {
  background-color: rgb(255, 255, 255);
  color: rgba(18, 18, 18, 0.9);
  padding-top: 0px;
  padding-bottom: 0px;
  padding-left: 0px;
  padding-right: 0px;
  position: static;
  box-shadow: rgba(18, 18, 18, 0.1) 10px 12px 20px 0px;
}
```

### Footer (27 instances)

```css
.foote {
  background-color: rgb(255, 255, 255);
  color: rgba(18, 18, 18, 0.9);
  padding-top: 0px;
  padding-bottom: 0px;
  font-size: 16px;
}
```

### Modals (29 instances)

```css
.modal {
  background-color: rgb(255, 255, 255);
  border-radius: 0px;
  padding-top: 0px;
  padding-right: 0px;
  max-width: 720px;
}
```

### Dropdowns (35 instances)

```css
.dropdown {
  background-color: rgb(255, 255, 255);
  border-radius: 0px;
  border-color: rgba(18, 18, 18, 0.9);
  padding-top: 0px;
}
```

### Badges (7 instances)

```css
.badge {
  background-color: rgb(255, 255, 255);
  color: rgb(255, 255, 255);
  font-size: 16px;
  font-weight: 400;
  padding-top: 0px;
  padding-right: 0px;
  border-radius: 0px;
}
```

### Avatars (3 instances)

```css
.avatar {
  border-radius: 50%;
}
```

### Tabs (3 instances)

```css
.tab {
  color: rgb(18, 18, 18);
  font-size: 13.3333px;
  font-weight: 400;
  padding-top: 6px;
  padding-right: 6px;
  border-color: rgb(18, 18, 18);
  border-radius: 50%;
}
```

### Accordions (76 instances)

```css
.accordion {
  color: rgba(18, 18, 18, 0.9);
  font-size: 16px;
  padding-top: 0px;
  padding-right: 0px;
  border-color: rgba(18, 18, 18, 0.9);
}
```

### Switches (10 instances)

```css
.switche {
  background-color: rgb(255, 255, 255);
  border-radius: 0px;
  border-color: rgba(18, 18, 18, 0.9);
}
```

## Component Clusters

Reusable component instances grouped by DOM structure and style similarity:

### Button — 4 instances, 1 variant

**Variant 1** (4 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(255, 255, 255);
  padding: 0px 30px 0px 30px;
  border-radius: 42px;
  border: 0px none rgb(255, 255, 255);
  font-size: 16px;
  font-weight: 700;
```

### Input — 2 instances, 1 variant

**Variant 1** (2 instances)

```css
  background: rgb(255, 255, 255);
  color: rgb(18, 18, 18);
  padding: 15px 98px 15px 15px;
  border-radius: 6px;
  border: 0px none rgb(18, 18, 18);
  font-size: 16px;
  font-weight: 400;
```

### Button — 10 instances, 3 variants

**Variant 1** (6 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgba(18, 18, 18, 0.9);
  font-size: 13.3333px;
  font-weight: 400;
```

**Variant 2** (2 instances)

```css
  background: rgb(18, 18, 18);
  color: rgba(255, 255, 255, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 50%;
  border: 0px none rgba(255, 255, 255, 0.9);
  font-size: 30px;
  font-weight: 400;
```

**Variant 3** (2 instances)

```css
  background: rgb(255, 255, 255);
  color: rgb(18, 18, 18);
  padding: 15px 40px 15px 21px;
  border-radius: 7px;
  border: 0px none rgb(18, 18, 18);
  font-size: 13px;
  font-weight: 400;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(18, 18, 18);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgb(18, 18, 18);
  font-size: 14px;
  font-weight: 400;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgb(51, 155, 67);
  color: rgb(255, 255, 255);
  padding: 0px 30px 0px 30px;
  border-radius: 42px;
  border: 0px none rgb(255, 255, 255);
  font-size: 18px;
  font-weight: 700;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(255, 255, 255);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgb(255, 255, 255);
  font-size: 18px;
  font-weight: 700;
```

### Button — 2 instances, 1 variant

**Variant 1** (2 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(18, 18, 18);
  padding: 1px 6px 1px 6px;
  border-radius: 0px;
  border: 0px none rgb(18, 18, 18);
  font-size: 13.3333px;
  font-weight: 400;
```

### Button — 2 instances, 1 variant

**Variant 1** (2 instances)

```css
  background: rgb(51, 155, 67);
  color: rgba(255, 255, 255, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 50%;
  border: 0px none rgba(255, 255, 255, 0.9);
  font-size: 13.3333px;
  font-weight: 400;
```

### Button — 6 instances, 1 variant

**Variant 1** (6 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(18, 18, 18);
  padding: 0px 0px 0px 0px;
  border-radius: 12px;
  border: 0px solid rgb(18, 18, 18);
  font-size: 13.3333px;
  font-weight: 400;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgba(18, 18, 18, 0.9);
  font-size: 16px;
  font-weight: 400;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(255, 255, 255);
  padding: 0px 30px 0px 30px;
  border-radius: 42px;
  border: 0px none rgb(255, 255, 255);
  font-size: 19px;
  font-weight: 700;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(255, 255, 255);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgb(255, 255, 255);
  font-size: 14px;
  font-weight: 700;
```

### Button — 4 instances, 2 variants

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(18, 18, 18);
  padding: 6px 6px 6px 6px;
  border-radius: 50%;
  border: 0px none rgb(18, 18, 18);
  font-size: 13.3333px;
  font-weight: 400;
```

**Variant 2** (1 instance)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(255, 255, 255);
  padding: 0px 30px 0px 30px;
  border-radius: 42px;
  border: 0px none rgb(255, 255, 255);
  font-size: 16px;
  font-weight: 700;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgb(255, 255, 255);
  color: rgba(18, 18, 18, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 24px;
  border: 0px solid rgba(18, 18, 18, 0.1);
  font-size: 16px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 24px;
  border: 0px none rgba(18, 18, 18, 0.9);
  font-size: 16px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgba(18, 18, 18, 0.9);
  font-size: 16px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 12.5px 20px 12.5px 20px;
  border-radius: 0px;
  border: 0px none rgba(18, 18, 18, 0.9);
  font-size: 16px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(255, 215, 0);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgb(255, 215, 0);
  font-size: 22px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgb(51, 155, 67);
  color: rgba(255, 255, 255, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 50%;
  border: 0px none rgba(255, 255, 255, 0.9);
  font-size: 50px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 10px 0px 0px 0px;
  border-radius: 0px;
  border: 1px 0px 0px solid none none rgba(18, 18, 18, 0.06) rgba(18, 18, 18, 0.9) rgba(18, 18, 18, 0.9);
  font-size: 16px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 50%;
  border: 0px none rgba(18, 18, 18, 0.9);
  font-size: 16px;
  font-weight: 400;
```

### Card — 3 instances, 1 variant

**Variant 1** (3 instances)

```css
  background: rgba(0, 0, 0, 0);
  color: rgba(18, 18, 18, 0.9);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgba(18, 18, 18, 0.9);
  font-size: 14px;
  font-weight: 400;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgba(0, 0, 0, 0);
  color: rgb(18, 18, 18);
  padding: 0px 0px 0px 0px;
  border-radius: 0px;
  border: 0px none rgb(18, 18, 18);
  font-size: 13.3333px;
  font-weight: 400;
```

### Button — 1 instance, 1 variant

**Variant 1** (1 instance)

```css
  background: rgb(255, 255, 255);
  color: rgb(18, 18, 18);
  padding: 0px 0px 0px 0px;
  border-radius: 50%;
  border: 1px solid rgba(18, 18, 18, 0.1);
  font-size: 13.3333px;
  font-weight: 400;
```

## Layout System

**16 grid containers** and **195 flex containers** detected.

### Container Widths

| Max Width | Padding |
|-----------|---------|
| 1400px | 50px |
| 1250px | 0px |
| 55% | 0px |
| 100% | 0px |
| 45% | 50px |
| 600px | 0px |
| 720px | 0px |
| 734px | 20px |

### Grid Column Patterns

| Columns | Usage Count |
|---------|-------------|
| 1-column | 14x |
| 3-column | 2x |

### Grid Templates

```css
grid-template-columns: 1280px;
grid-template-columns: 366.656px 366.672px 366.656px;
gap: 40px;
grid-template-columns: 400px;
grid-template-columns: 483.75px 172.5px 483.75px;
gap: normal 20px;
grid-template-columns: 481px;
```

### Flex Patterns

| Direction/Wrap | Count |
|----------------|-------|
| row/nowrap | 159x |
| row/wrap | 15x |
| column/nowrap | 18x |
| row-reverse/wrap | 2x |
| column/wrap | 1x |

**Gap values:** `10px`, `10px normal`, `40px`, `40px normal`, `5px`, `60px 0px`, `8px`, `normal 100px`, `normal 10px`, `normal 16px`, `normal 20px`, `normal 3.9px`, `normal 30px`

## Responsive Design

### Viewport Snapshots

| Viewport | Body Font | Nav Visible | Max Columns | Hamburger | Page Height |
|----------|-----------|-------------|-------------|-----------|-------------|
| mobile (375px) | 15px | Yes | 3 | Yes | 8264px |
| tablet (768px) | 16px | Yes | 3 | Yes | 6897px |
| desktop (1280px) | 16px | Yes | 3 | Yes | 6324px |
| wide (1920px) | 16px | Yes | 3 | Yes | 6406px |

### Breakpoint Changes

**375px → 768px** (mobile → tablet):
- Body font size: `15px` → `16px`
- Page height: `8264px` → `6897px`

**768px → 1280px** (tablet → desktop):
- Page height: `6897px` → `6324px`

## Interaction States

### Button States

**""**
```css
/* Focus */
box-shadow: none → rgba(18, 18, 18, 0.3) 0px 0px 2px 0px;
outline: rgb(18, 18, 18) none 3px → rgba(18, 18, 18, 0.5) solid 2px;
```

**"Cart"**
```css
/* Hover */
text-decoration: none → underline;
```
```css
/* Focus */
box-shadow: none → rgba(18, 18, 18, 0.3) 0px 0px 2px 0px;
outline: rgb(18, 18, 18) none 3px → rgba(18, 18, 18, 0.5) solid 2px;
text-decoration: none → underline;
```

### Link Hover

```css
color: rgba(18, 18, 18, 0.9) → rgb(51, 155, 67);
border-color: rgba(18, 18, 18, 0.9) → rgb(51, 155, 67);
outline: rgba(18, 18, 18, 0.9) none 3px → rgb(51, 155, 67) none 3px;
```

### Input Focus

```css
box-shadow: none → rgb(46, 42, 57) 0px 0px 0px 1px;
outline: rgb(46, 42, 57) none 3px → rgb(46, 42, 57) none 0px;
```

## Accessibility (WCAG 2.1)

**Overall Score: 100%** — 3 passing, 0 failing color pairs

### Passing Color Pairs

| Foreground | Background | Ratio | Level |
|------------|------------|-------|-------|
| `#ffffff` | `#2d5f3f` | 7.45:1 | AAA |
| `#ffffff` | `#121212` | 18.73:1 | AAA |
| `#121212` | `#ffffff` | 18.73:1 | AAA |

## Design System Score

**Overall: 78/100 (Grade: C)**

| Category | Score |
|----------|-------|
| Color Discipline | 92/100 |
| Typography Consistency | 40/100 |
| Spacing System | 85/100 |
| Shadow Consistency | 100/100 |
| Border Radius Consistency | 80/100 |
| Accessibility | 100/100 |
| CSS Tokenization | 100/100 |

**Strengths:** Tight, disciplined color palette, Well-defined spacing scale, Clean elevation system, Strong accessibility compliance, Good CSS variable tokenization

**Issues:**
- 7 font families — consider limiting to 2 (heading + body)
- 26 distinct font sizes — consider a tighter type scale
- 72 !important rules — prefer specificity over overrides
- 79% of CSS is unused — consider purging
- 5679 duplicate CSS declarations

## Gradients

**2 unique gradients** detected.

| Type | Direction | Stops | Classification |
|------|-----------|-------|----------------|
| linear | — | 2 | brand |
| linear | 135deg | 2 | brand |

```css
background: linear-gradient(rgba(18, 18, 18, 0.04), rgba(18, 18, 18, 0.04));
background: linear-gradient(135deg, rgb(51, 155, 67) 0%, rgb(112, 185, 123) 100%);
```

## Z-Index Map

**13 unique z-index values** across 3 layers.

| Layer | Range | Elements |
|-------|-------|----------|
| modal | 1000,2147483647 | cart-drawer.d.r.a.w.e.r. .i.s.-.e.m.p.t.y. .c.a.r.t.-.d.r.a.w.e.r.-.-.d.e.s.k.t.o.p.-.w.i.d.t.h.-.n.o.r.m.a.l. .c.a.r.t.-.d.r.a.w.e.r.-.-.m.o.b.i.l.e.-.w.i.d.t.h.-.p.a.r.t.i.a.l, div.f.i.x.e.d. .i.n.s.e.t.-.0. .z.-.m.a.x. .o.v.e.r.f.l.o.w.-.h.i.d.d.e.n. .f.l.e.x. .i.t.e.m.s.-.c.e.n.t.e.r. .j.u.s.t.i.f.y.-.c.e.n.t.e.r. .p.o.i.n.t.e.r.-.e.v.e.n.t.s.-.n.o.n.e. .i.n.v.i.s.i.b.l.e, div.w.h.o.o.p. .r.m.z.-.c.h.a.t.-.b.u.b.b.l.e |
| sticky | 10,50 | div.g.r.a.d.i.e.n.t. .m.e.n.u.-.d.r.a.w.e.r. .m.o.t.i.o.n.-.r.e.d.u.c.e. .c.o.l.o.r.-.b.a.c.k.g.r.o.u.n.d.-.1, div.f.i.x.e.d. .i.n.s.e.t.-.0. .z.-.1.0. .b.g.-.o.v.e.r.l.a.y. .t.r.a.n.s.i.t.i.o.n.-.o.p.a.c.i.t.y. .d.u.r.a.t.i.o.n.-.4.0.0. .e.a.s.e.-.c.u.b.i.c.-.m.o.d.a.l. .m.o.t.i.o.n.-.r.e.d.u.c.e._.d.u.r.a.t.i.o.n.-.0. .o.p.a.c.i.t.y.-.0, section.r.e.l.a.t.i.v.e. .z.-.5.0. .b.g.-.w.h.i.t.e. .t.r.a.n.s.i.t.i.o.n. .d.u.r.a.t.i.o.n.-.4.0.0. .e.a.s.e.-.c.u.b.i.c.-.m.o.d.a.l. .w.i.l.l.-.c.h.a.n.g.e.-.t.r.a.n.s.f.o.r.m. .f.o.c.u.s._.o.u.t.l.i.n.e.-.n.o.n.e. .f.o.c.u.s._.o.u.t.l.i.n.e.-.0. .m.o.t.i.o.n.-.r.e.d.u.c.e._.d.u.r.a.t.i.o.n.-.0. .s.m._.a.b.s.o.l.u.t.e. .s.m._.i.n.s.e.t.-.x.-.0. .s.m._.b.o.t.t.o.m.-.0. .s.m._.t.o.p.-.a.u.t.o. .s.m._.r.o.u.n.d.e.d.-.b.-.n.o.n.e. .o.p.a.c.i.t.y.-.0. .s.m._.t.r.a.n.s.l.a.t.e.-.y.-.f.u.l.l. .m.i.n.-.w.-.8.5. .r.o.u.n.d.e.d.-.x.x.l |
| base | -100,5 | div, div.a.b.s.o.l.u.t.e. .i.n.s.e.t.-.0.5. .-.z.-.1.0. .r.o.u.n.d.e.d.-.m.a.x. .b.g.-.g.r.a.y.s.c.a.l.e.-.p.r.i.m.a.r.y.-.l.i.g.h.t, product-modal.p.r.o.d.u.c.t.-.m.e.d.i.a.-.m.o.d.a.l. .m.e.d.i.a.-.m.o.d.a.l |

**Issues:**
- [object Object]

## SVG Icons

**26 unique SVG icons** detected. Dominant style: **filled**.

| Size Class | Count |
|------------|-------|
| xs | 3 |
| sm | 3 |
| md | 6 |
| lg | 13 |
| xl | 1 |

**Icon colors:** `rgb(0, 0, 0)`, `currentColor`, `#fff`, `#142688`, `#EB001B`, `#F79E1B`, `#FF5F00`, `#000`, `#006FCF`, `#FFF`

## Font Files

| Family | Source | Weights | Styles |
|--------|--------|---------|--------|
| Montserrat | self-hosted | 400, 600, 700 | normal, italic |
| Material Symbols Outlined | cdn | 300 | normal |
| GTStandard-M | self-hosted | 450, 500, 600 | normal |
| InterVariable | self-hosted | 100 900 | normal |

## Image Style Patterns

| Pattern | Count | Key Styles |
|---------|-------|------------|
| thumbnail | 62 | objectFit: contain, borderRadius: 0px, shape: square |
| general | 12 | objectFit: cover, borderRadius: 12px, shape: rounded |
| hero | 5 | objectFit: cover, borderRadius: 12px, shape: rounded |

**Aspect ratios:** 1:1 (34x), 3:2 (26x), 2.88:1 (4x), 5.16:1 (4x), 21:9 (4x), 3.48:1 (4x), 3.65:1 (1x), 4:3 (1x)

## Motion Language

**Feel:** responsive · **Scroll-linked:** yes

### Duration Tokens

| name | value | ms |
|---|---|---|
| `xs` | `100ms` | 100 |
| `sm` | `200ms` | 200 |
| `md` | `300ms` | 300 |
| `lg` | `450ms` | 450 |
| `xl` | `750ms` | 750 |
| `xxl` | `1.35s` | 1350 |

### Easing Families

- **ease-in-out** (33 uses) — `ease`
- **ease-out** (35 uses) — `cubic-bezier(0.25, 0.46, 0.45, 0.94)`, `cubic-bezier(0.32, 0.72, 0, 1)`
- **custom** (1 uses) — `cubic-bezier(0.4, 0, 0.2, 1)`

### Keyframes In Use

| name | kind | properties | uses |
|---|---|---|---|
| `rotator` | rotate | transform | 2 |
| `dash` | rotate | stroke-dashoffset, transform | 2 |
| `move-forever1` | slide | transform | 2 |
| `move-forever2` | slide | transform | 2 |
| `move-forever3` | slide | transform | 2 |
| `move-forever4` | slide | transform | 2 |
| `animateLocalization` | slide-y | opacity, transform | 1 |
| `desktopHorTickersections--19451233698020__horizontal_ticker_4U3wL7` | slide | transform | 1 |
| `desktopHorTickertemplate--19451233599716__horizontal_ticker_nYpqJK` | slide | transform | 1 |
| `desktopHorTickersections--19451233665252__horizontal_ticker_DzgrVq` | slide | transform | 1 |
| `whoop` | scale | transform | 1 |
| `whoop` | scale | transform | 1 |
| `toothpaste` | fade | opacity | 1 |
| `toothpaste` | fade | opacity | 1 |

## Component Anatomy

### button — 36 instances

**Slots:** label
**Variants:** link · primary
**Sizes:** large

| variant | count | sample label |
|---|---|---|
| default | 30 | Continue shopping |
| link | 5 | Skip to content |
| primary | 1 | ADD TO CART |

### card — 27 instances

**Slots:** media

### input — 2 instances


## Brand Voice

**Tone:** friendly · **Pronoun:** you-only · **Headings:** Title Case (balanced)

### Top CTA Verbs

- **add** (4)
- **skip** (2)
- **check** (2)
- **cart** (1)
- **continue** (1)
- **sign** (1)
- **united** (1)

### Button Copy Patterns

- "add to cart" (4×)
- "check out" (2×)
- "skip to content" (1×)
- "cart" (1×)
- "continue shopping" (1×)
- "skip to product information" (1×)
- "sign up" (1×)
- "united states (usd $)" (1×)

### Sample Headings

> Menu
> Vet-Approved Benefits
> Free Shipping
> 90-Day Refund No Question Asked
> Make Every Meal Last 10X Longer For A Healthy Life
> Transforms Dangerous Gulping into Healthy Eating
> Vet-Approved Benefits
> Free Shipping
> 90-Day Refund No Question Asked
> Vet-Approved Benefits

## Page Intent

**Type:** `product` (confidence 0.75)

## Section Roles

Reading order (top→bottom): pricing-table → pricing-table → pricing-table → nav → nav → nav → content → testimonial → testimonials → cta → footer

| # | Role | Heading | Confidence |
|---|------|---------|------------|
| 0 | nav | Menu | 0.4 |
| 1 | nav | — | 0.9 |
| 2 | nav | — | 0.9 |
| 3 | pricing-table | Vet-Approved Benefits | 0.9 |
| 4 | pricing-table | Vet-Approved Benefits | 0.9 |
| 5 | pricing-table | Vet-Approved Benefits | 0.9 |
| 6 | content | — | 0.3 |
| 7 | testimonial | Real Stories From Dog Moms Who Transformed Mealtime | 0.8 |
| 8 | testimonials | FAQs | 0.4 |
| 9 | cta | Join the Waggier Pack! | 0.75 |
| 10 | footer | Need Help? | 0.95 |

## Material Language

**Label:** `flat` (confidence 0)

| Metric | Value |
|--------|-------|
| Avg saturation | 0.292 |
| Shadow profile | soft |
| Avg shadow blur | 0px |
| Max radius | 999px |
| backdrop-filter in use | no |
| Gradients | 2 |

## Imagery Style

**Label:** `photography` (confidence 0.215)
**Counts:** total 79, svg 26, icon 32, screenshot-like 0, photo-like 20
**Dominant aspect:** square-ish
**Radius profile on images:** square

## Multi-Page Map

| Page Type | URL | Status |
|-----------|-----|--------|
| auth | https://waggier.com/customer_authentication/redirect?locale=en&region_country=US | ok |

## Component Screenshots

8 retina crops written to `screenshots/`. Index: `*-screenshots.json`.

| Cluster | Variant | Size (px) | File |
|---------|---------|-----------|------|
| button--default | 0 | 124 × 49 | `screenshots/button-default-0.png` |
| button--default | 1 | 44 × 44 | `screenshots/button-default-1.png` |
| input--default | 0 | 358 × 45 | `screenshots/input-default-0.png` |
| card--default | 0 | 367 × 367 | `screenshots/card-default-0.png` |
| card--default | 1 | 367 × 367 | `screenshots/card-default-1.png` |
| card--default | 2 | 367 × 397 | `screenshots/card-default-2.png` |
| button--primary | 0 | 187 × 49 | `screenshots/button-primary-0.png` |
| button--default--large | 0 | 209 × 42 | `screenshots/button-default-large-0.png` |

Full-page: `screenshots/full-page.png`

## Quick Start

To recreate this design in a new project:

1. **Install fonts:** Add `Montserrat` from Google Fonts or your font provider
2. **Import CSS variables:** Copy `variables.css` into your project
3. **Tailwind users:** Use the generated `tailwind.config.js` to extend your theme
4. **Design tokens:** Import `design-tokens.json` for tooling integration
