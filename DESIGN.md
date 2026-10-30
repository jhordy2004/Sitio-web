---
name: Crimson Ink
colors:
  surface: '#f3fcf0'
  surface-dim: '#d4ddd1'
  surface-bright: '#f3fcf0'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#edf6ea'
  surface-container: '#e7f0e5'
  surface-container-high: '#e2ebdf'
  surface-container-highest: '#dce5d9'
  on-surface: '#161d16'
  on-surface-variant: '#5b403f'
  inverse-surface: '#2a322b'
  inverse-on-surface: '#eaf3e7'
  outline: '#8f6f6e'
  outline-variant: '#e4bebc'
  surface-tint: '#bb152c'
  primary: '#b7102a'
  on-primary: '#ffffff'
  primary-container: '#db313f'
  on-primary-container: '#fffbff'
  inverse-primary: '#ffb3b1'
  secondary: '#485f84'
  on-secondary: '#ffffff'
  secondary-container: '#bbd3fd'
  on-secondary-container: '#445a7f'
  tertiary: '#286182'
  on-tertiary: '#ffffff'
  tertiary-container: '#447a9c'
  on-tertiary-container: '#fcfcff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#ffdad8'
  primary-fixed-dim: '#ffb3b1'
  on-primary-fixed: '#410007'
  on-primary-fixed-variant: '#92001c'
  secondary-fixed: '#d5e3ff'
  secondary-fixed-dim: '#b0c7f1'
  on-secondary-fixed: '#001b3c'
  on-secondary-fixed-variant: '#30476a'
  tertiary-fixed: '#c7e7ff'
  tertiary-fixed-dim: '#98cdf2'
  on-tertiary-fixed: '#001e2e'
  on-tertiary-fixed-variant: '#064c6b'
  background: '#f3fcf0'
  on-background: '#161d16'
  surface-variant: '#dce5d9'
typography:
  display-lg:
    fontFamily: Anton
    fontSize: 72px
    fontWeight: '400'
    lineHeight: '1.1'
    letterSpacing: 0.02em
  headline-lg:
    fontFamily: Anton
    fontSize: 48px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Anton
    fontSize: 32px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Anton
    fontSize: 24px
    fontWeight: '400'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Hanken Grotesk
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Hanken Grotesk
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.2'
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 8px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 64px
  max-width: 1440px
---

## Brand & Style

This design system is built for a vibrant, high-energy Manga marketplace. It fuses the raw, kinetic energy of print manga with a modern, high-contrast digital interface. The brand personality is bold, authoritative, and deeply rooted in comic culture, yet refined enough for a seamless e-commerce experience.

The visual style is **Bold / Modern** with a "Manga-Industrial" twist. We employ clean lines and high-contrast surfaces to ensure readability, while integrating subtle halftone and screentone patterns in backgrounds to pay homage to traditional ink-and-paper manga production. The interface should feel fast, punchy, and collectibles-focused, evoking the excitement of a new release day at a flagship bookstore.

## Colors

The palette is driven by the classic "Ink and Blood" aesthetic common in seinen and shonen manga.

- **Primary (#E63946):** A high-impact crimson used for "Add to Cart" actions, price badges, and critical UI highlights. It demands attention and drives conversion.
- **Secondary/Ink (#1D3557):** A deep, saturated ink black. Used for headers, primary typography, and structural borders. It provides a heavy, grounded contrast to the red.
- **Base/Paper (#F1FAEE):** A clean, off-white "paper" tone. This serves as the primary background color, reducing eye strain compared to pure white and providing a tactile, book-like feel.
- **Screentone Pattern:** Utilize a 5% opacity version of the Ink color for subtle halftone dot patterns in section backgrounds or card hover states to reinforce the print theme.

## Typography

Typography in this design system is split between "Impact" and "Precision."

- **Headlines:** We use **Anton** for all major headings. Its condensed, bold nature mirrors the punchy sound effects and title cards found in manga. Use it sparingly for maximum impact.
- **Body Text:** **Hanken Grotesk** provides a clean, contemporary feel that ensures high legibility for book descriptions and reviews. It balances the aggression of the headlines with a professional air.
- **Metadata & Labels:** **JetBrains Mono** is used for technical data like ISBNs, page counts, and price badges. The monospaced nature suggests a "cataloging" or "archival" aesthetic appropriate for collectors.

## Layout & Spacing

The layout follows a **Fixed Grid** model on desktop to mimic the structured nature of manga panels.

- **Grid:** A 12-column grid with a 24px gutter. Elements should align strictly to these grid lines to maintain a "panel-like" structure.
- **Margins:** Generous 64px margins on desktop provide room for the "screentone" background patterns to breathe.
- **Panel Logic:** Use variable height containers for manga volume cards to create a rhythmic, masonry-style look in lists, but maintain strict horizontal alignment for section headers.
- **Responsive:** On mobile, collapse to a 2-column "vertical scroll" grid for volume listings to ensure cover art remains legible.

## Elevation & Depth

We avoid soft, blurry shadows in favor of **Tonal Layers and Bold Borders.**

- **Structural Depth:** Depth is created through a "Stacking" metaphor. Surfaces do not float; they sit on top of each other with crisp, 1px or 2px solid Ink (#1D3557) borders.
- **Shadows:** If shadows are used, they are "Hard Shadows"—solid offsets of the Ink color (e.g., 4px 4px 0px #1D3557) rather than soft blurs. This mimics comic book shading.
- **Interactive State:** Hovering over a card should trigger a 4px offset "pop" effect, moving the element up and left while the hard shadow remains fixed.

## Shapes

The shape language is primarily **Sharp**, with intentional, localized rounding for interactive elements.

- **Containers & Cards:** 0px radius. Crisp corners reinforce the "panel" aesthetic.
- **Buttons & Chips:** 4px radius (Soft). This slight rounding provides a tactile target for the user and distinguishes "clickable" actions from "informational" panels.
- **Image Treatment:** Manga covers must remain sharp-cornered.

## Components

### Manga Volume Cards
Vertical orientation (2:3 aspect ratio). The cover art is the hero, framed by a 1px Ink border. The title uses `headline-md` and the price is housed in a `label-sm` badge with a Primary Red background.

### Primary Buttons (Add to Cart)
Bold, rectangular buttons with a Primary Red (#E63946) fill and White (#F1FAEE) text. They feature a subtle 2px bottom-heavy border in the Secondary Ink color to simulate weight.

### Price Badges
High-contrast labels using **JetBrains Mono**. These should be positioned in the top-right corner of cards or immediately adjacent to titles, using a solid background color to "pop" off the paper base.

### Screentone Backgrounds
Used specifically for "Hero" sections or site-wide backgrounds. A repeating dot-grid pattern at 5% opacity of the Ink color.

### Input Fields
Clean, white backgrounds with a 2px solid Ink border. Focus states change the border to Primary Red. No rounded corners for inputs.