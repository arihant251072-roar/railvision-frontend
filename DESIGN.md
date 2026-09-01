---
name: Kinetic Industrial Console
colors:
  surface: '#10131a'
  surface-dim: '#10131a'
  surface-bright: '#363940'
  surface-container-lowest: '#0b0e14'
  surface-container-low: '#191c22'
  surface-container: '#1d2026'
  surface-container-high: '#272a31'
  surface-container-highest: '#32353c'
  on-surface: '#e1e2eb'
  on-surface-variant: '#c7c4d8'
  inverse-surface: '#e1e2eb'
  inverse-on-surface: '#2e3037'
  outline: '#918fa1'
  outline-variant: '#464555'
  surface-tint: '#c3c0ff'
  primary: '#c3c0ff'
  on-primary: '#1d00a5'
  primary-container: '#4f46e5'
  on-primary-container: '#dad7ff'
  inverse-primary: '#4d44e3'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffb95f'
  on-tertiary: '#472a00'
  tertiary-container: '#885500'
  on-tertiary-container: '#ffd4a4'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e2dfff'
  primary-fixed-dim: '#c3c0ff'
  on-primary-fixed: '#0f0069'
  on-primary-fixed-variant: '#3323cc'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffddb8'
  tertiary-fixed-dim: '#ffb95f'
  on-tertiary-fixed: '#2a1700'
  on-tertiary-fixed-variant: '#653e00'
  background: '#10131a'
  on-background: '#e1e2eb'
  surface-variant: '#32353c'
typography:
  display-lg:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  data-lg:
    fontFamily: JetBrains Mono
    fontSize: 20px
    fontWeight: '500'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.05em
  code-sm:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  gutter: 16px
  margin: 24px
  container-padding: 12px
---

## Brand & Style
The design system is engineered for high-stakes railway infrastructure monitoring. It adopts a **Technical Minimalism** style, blending the precision of aerospace telemetry with the clarity of modern enterprise software. The personality is authoritative, vigilant, and mission-critical.

The interface prioritizes information density and operational speed. It utilizes a "Dark Mode First" philosophy to reduce eye strain in control room environments, using subtle luminous accents to guide the operator's eye to anomalies and critical data points.

## Colors
The palette is rooted in a deep, "Near-Black" obsidian base to provide maximum contrast for data visualization. 

- **Core Tones**: The background uses `#0B0E14`, while interactive surfaces and card containers use `#1A1D23`. 
- **Functional Accents**: Indigo is reserved for navigational focus and brand identity. 
- **Diagnostic Logic**: A strict semantic color system is applied to all data points:
    - **Healthy**: Emerald for nominal operations.
    - **Degrading**: Amber for preventative maintenance alerts.
    - **Critical**: Vivid Red for immediate attention.
    - **Emergency**: Pure Red, often paired with a subtle glow or pulse animation for catastrophic failures.

## Typography
This design system employs a dual-font strategy:
1. **Inter** is used for the structural UI, navigation, and general communication to ensure a modern, approachable feel.
2. **JetBrains Mono** is utilized for all telemetry, timestamps, coordinates, and sensor readings. The monospaced nature ensures that fluctuating numbers do not cause "jitter" in the layout.

For mobile views, `display-lg` scales down to 24px to maintain readability without overwhelming the viewport. All labels in the dashboard should use `label-caps` for a distinct "instrumentation" aesthetic.

## Layout & Spacing
The layout follows a **High-Density Fluid Grid**. It utilizes a 12-column system for desktop views, collapsing to 4 columns on mobile. 

- **Modular Rhythm**: Spacing is based on a 4px baseline grid.
- **Density**: Vertical rhythm is tight (12px - 16px padding inside cards) to maximize the amount of visible data on a single screen without requiring excessive scrolling.
- **Reflow**: On tablet devices, sidebars collapse into icons to prioritize the central diagnostic charts. On mobile, charts stack vertically, and data tables transition into condensed list cards.

## Elevation & Depth
Depth is conveyed through **Tonal Layering** and **Subtle Outlines** rather than heavy shadows, ensuring the UI feels crisp and digital.

- **Level 0 (Canvas)**: `#0B0E14` - The deepest layer.
- **Level 1 (Cards/Panels)**: `#1A1D23` with a 1px border of `#2D3139`. 
- **Level 2 (Popovers/Tooltips)**: `#242830` with a soft 8px blur shadow.

**Status Glows**: Elements with critical status (Red/Amber) utilize a 4px outer glow (drop-shadow with 0 offset) using the semantic color at 30% opacity to simulate a glowing physical indicator light.

## Shapes
The design system uses a **Rounded** language (8px - 12px) to soften the industrial nature of the data. 

- **Primary Components**: Buttons and Input fields use the standard `0.5rem` (8px) radius.
- **Data Containers**: Large dashboard cards use `rounded-lg` (16px) to create clear visual separation between distinct metric groups.
- **Status Pills**: Small diagnostic chips and status indicators use the "Pill" shape for immediate recognition.

## Components
- **Buttons**: Primary buttons are solid Indigo. Secondary buttons are ghost-style with a thin `#2D3139` border.
- **Diagnostic Chips**: Small, monospaced labels used for sensor tags. They feature a left-hand "indicator dot" that pulses when data is live.
- **Data Tables**: High-density rows with alternating "Zebra" striping using a 2% lighter background. Borders are horizontal only.
- **Sparklines**: Integrated into list views to show 24-hour trends without full-scale charts.
- **Input Fields**: Dark backgrounds (`#0B0E14`) with a 1px border. Focus state changes the border to Indigo with a subtle inner glow.
- **Status Badges**: Semi-transparent background of the semantic color (15% opacity) with a fully opaque border and text for maximum visibility.
- **Telemetry Cards**: Specific components that feature a large JetBrains Mono value, a percentage change indicator, and a background subtle histogram.