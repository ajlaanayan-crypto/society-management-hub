---
name: Luminous Tactility
colors:
  surface: '#fbf9f9'
  surface-dim: '#dbdad9'
  surface-bright: '#fbf9f9'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f5f3f3'
  surface-container: '#efeded'
  surface-container-high: '#e9e8e7'
  surface-container-highest: '#e3e2e2'
  on-surface: '#1b1c1c'
  on-surface-variant: '#444748'
  inverse-surface: '#303031'
  inverse-on-surface: '#f2f0f0'
  outline: '#747878'
  outline-variant: '#c4c7c7'
  surface-tint: '#5f5e5e'
  primary: '#2c2c2c'
  on-primary: '#ffffff'
  primary-container: '#424242'
  on-primary-container: '#b0aeae'
  inverse-primary: '#c8c6c6'
  secondary: '#5f5e5e'
  on-secondary: '#ffffff'
  secondary-container: '#e5e2e1'
  on-secondary-container: '#656464'
  tertiary: '#2f2b2b'
  on-tertiary: '#ffffff'
  tertiary-container: '#454141'
  on-tertiary-container: '#b3adad'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e4e2e1'
  primary-fixed-dim: '#c8c6c6'
  on-primary-fixed: '#1b1c1c'
  on-primary-fixed-variant: '#474747'
  secondary-fixed: '#e5e2e1'
  secondary-fixed-dim: '#c8c6c5'
  on-secondary-fixed: '#1c1b1b'
  on-secondary-fixed-variant: '#474646'
  tertiary-fixed: '#e8e1e0'
  tertiary-fixed-dim: '#ccc5c5'
  on-tertiary-fixed: '#1e1b1b'
  on-tertiary-fixed-variant: '#4a4646'
  background: '#fbf9f9'
  on-background: '#1b1c1c'
  surface-variant: '#e3e2e2'
typography:
  headline-lg:
    fontFamily: Manrope
    fontSize: 48px
    fontWeight: '800'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-lg-mobile:
    fontFamily: Manrope
    fontSize: 32px
    fontWeight: '800'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Manrope
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
  headline-sm:
    fontFamily: Manrope
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
  body-lg:
    fontFamily: Manrope
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Manrope
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-md:
    fontFamily: Manrope
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-sm:
    fontFamily: Manrope
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.02em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 12px
  md: 24px
  lg: 48px
  xl: 80px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 64px
---

## Brand & Style

The design system focuses on a tactile, soft-UI aesthetic that mimics physical extrusion and indentation. By utilizing a monochromatic light grey palette, the interface achieves a "clay-molded" appearance that feels organic and calm. The target audience values a premium, serene digital environment that prioritizes sensory-like depth over traditional flat interfaces.

The design style is **Neomorphism**. It relies on precise shadow orchestration—using light and dark offsets—to create the illusion that UI elements are pushed out from or pressed into the background surface. The emotional response is one of softness, approachability, and high-end craftsmanship.

## Colors

The palette is strictly functional to support the neomorphic effect. The base color for both the background and surface elements is a consistent light grey (#e0e0e0), ensuring that depth is created through lighting rather than color shifts.

- **Primary/Text**: Dark grey (#424242) ensures accessibility and high legibility against the light grey background.
- **Highlights**: Pure white (#ffffff) is used for top-left shadows to simulate a light source.
- **Shadows**: A muted mid-grey (#bebebe) provides the bottom-right depth.
- **Accents**: Use subtle opacity shifts of the primary dark grey for secondary information.

## Typography

This design system utilizes **Manrope** across all levels to maintain a modern, geometric, and highly readable look. The typography is treated as a high-contrast layer floating above the tactile surfaces.

Headlines use heavy weights and tight letter-spacing to command attention against the soft UI. Body text maintains generous line heights to ensure long-form readability. For mobile devices, headline sizes are scaled down to prevent excessive wrapping while maintaining their bold character.

## Layout & Spacing

The layout follows a fluid 12-column grid for desktop and a 4-column grid for mobile. Because neomorphic elements require significant "breathing room" for their shadows to be visible without clipping, the spacing rhythm is generous.

- **Internal Padding**: Elements should have at least 24px of internal padding to ensure the "extrusion" feels substantial.
- **Margins**: Use the 8px base unit. Component-to-component spacing should lean toward 'md' (24px) or 'lg' (48px) to prevent the soft shadows from overlapping and becoming muddy.
- **Alignment**: Center-aligned layouts are preferred for marketing or simple tool interfaces to emphasize the symmetry of the tactile shapes.

## Elevation & Depth

Elevation is not achieved through Z-index stacking but through **dual-source shadowing**. All "raised" elements must use two shadows:
1. **Top-Left**: #ffffff, Blur: 10px to 20px, Offset: -5px to -10px.
2. **Bottom-Right**: #bebebe, Blur: 10px to 20px, Offset: 5px to 10px.

For "pressed" or "sunken" states (like active buttons or input fields), the shadows are moved inside the element using `inset`. The background color of the element remains #e0e0e0 to maintain the illusion that the surface is continuous and merely deformed.

## Shapes

The design system uses a consistent **8px (0.5rem)** base radius for standard components, which aligns with the "ROUND_EIGHT" requirement. 

- **Standard Elements**: 8px (0.5rem) radius creates a soft but defined look.
- **Large Containers/Cards**: 16px (1rem) radius (rounded-lg) to accommodate larger shadow spreads.
- **Extra Large Sections**: 24px (1.5rem) radius (rounded-xl) for hero areas.

Avoid sharp 0px corners, as they break the organic, liquid-tension illusion of the neomorphic style.

## Components

### Buttons
Buttons appear extruded from the background. On hover, the shadow intensity increases slightly. On click/active, the button transitions to an `inset` shadow state, appearing physically pressed into the surface. Text remains #424242.

### Input Fields
Inputs should default to the `inset` (sunken) state to indicate a valley where data can be placed. Use a 1px subtle stroke of #bebebe only if extra definition is needed for accessibility.

### Cards
Cards are the primary layout container. They use the standard dual-shadow extrusion. Card headers should be separated by whitespace rather than lines to maintain the "molded" aesthetic.

### Chips & Tags
Small pill-shaped extrusions. These can use a primary-colored text (#424242) or a subtle background tint of #d0d0d0 if they need to stand out from the main surface.

### Lists
List items should be flat against the surface, separated by subtle indentations or simple horizontal space. Avoid wrapping every list item in an extruded box to prevent "visual noise" overload.