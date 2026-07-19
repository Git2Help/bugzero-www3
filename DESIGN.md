---
version: alpha
name: BugZero IT Support Landing Page Template
description: A retro-inspired, high-contrast IT support landing page featuring a "pixel-art" aesthetic, hard shadows, and a grid-based structural rhythm.
colors:
  primary: "#0ba5dc"
  secondary: "#c8d900"
  accent-yellow: "#fbbf24"
  accent-red: "#ef4444"
  accent-purple: "#a855f7"
  accent-green: "#22c55e"
  accent-pink: "#ec4899"
  neutral-900: "#171717"
  neutral-100: "#f5f5f5"
  grid-line: "#f0f0f0"
typography:
  headings: "VT323, monospace"
  body: "Inter, sans-serif"
  base-size: 16px
spacing:
  grid-gap: 40px
  section-padding: 96px
rounded:
  default: 0px
  cards: 8px
components:
  button-primary: "bg-yellow-400 border-2 border-black shadow-hard"
  card-service: "border-2 border-black shadow-hard-sm"
  navbar: "backdrop-blur-md border-b-2"
---

## Overview
BugZero is a high-energy, retro-styled landing page for IT support services. The visual personality is defined by a "pixel-art" and gaming-adjacent aesthetic, using the VT323 monospaced font to evoke 80s/90s computing. The interface is high-density and tactile, utilizing "hard" shadows (non-blurred, offset black rectangles) and a persistent 40px background grid. The tone is professional yet approachable, using vibrant primary and secondary colors against a clean white and neutral-50 background.

## Colors
- **Primary Blue (#0ba5dc)**: Used in branding and icon accents.
- **Secondary Lime (#c8d900)**: Used in branding and logo highlights.
- **Status/Service Colors**:
  - Red (#ef4444): Warnings and Phone Setup service.
  - Purple (#a855f7): Gaming/Custom PC service.
  - Green (#22c55e): Wi-Fi and connectivity.
  - Pink (#ec4899): Server/NAS and Social links.
- **Backgrounds**: Pure white (#ffffff) with a light gray grid (#f0f0f0); off-white (#fafafa) for sections.
- **Text**: Neutral-900 for high readability.

## Typography
- **Font-Pixel (VT323)**: Monospaced, used for all major headings, navigation links, and button text. Highly expressive and retro.
- **Font-Sans (Inter)**: Clean sans-serif used for body copy, descriptions, and small metadata to ensure legibility.
- **Hierarchy**:
  - Hero Title: font-pixel, 6xl to 8xl.
  - Section Headers: font-pixel, 6xl.
  - Body Text: font-sans, text-xl/text-lg.

## Layout
- **Grid Background**: A fixed 40px x 40px linear gradient grid pattern applied to the body.
- **Max Width**: Content is contained within a max-width of 1280px (7xl).
- **Responsive Strategy**: Single-column layout on mobile, transitioning to 2-column (Hero) or 4-column (Services) grids on desktop.
- **Z-Index Stack**: Floating background icons (z-0), sticky navbar (z-50), and main content (z-10).

## Elevation & Depth
- **Hard Shadows**: Instead of standard soft shadows, the site uses `4px 4px 0px 0px rgba(0,0,0,1)`.
- **Interaction Elevation**: On hover, shadows increase to `6px` and the element translates `-2px`. On active/click, shadows disappear and the element translates `4px` to simulate a physical button press.
- **Backdrop Blur**: Navigation uses `backdrop-blur-md` with 90% opacity white for a glass-like feel over the background grid.

## Shapes
- **Strict Geometry**: Most components (buttons, badges) have zero border-radius (`rounded-none`).
- **Card Variation**: The central "Hero Card" (Tablet) and service icons use a small radius (`rounded-lg` or `rounded-none`) to maintain the blocky, retro feel.
- **Accents**: Rectangular blocks and border-based separators.

## Components
- **Navbar**: Sticky top bar with logo on the left and pixel-font navigation links on the right. Contact button follows the "hard shadow" design.
- **Buttons**: Two primary styles—Solid color (Yellow/White) with 2px black borders and hard shadows.
- **Service Cards**: Square or rectangular blocks with thick 2px borders, individual background colors (Red, Purple, Green, Blue, Pink), and centered Lucide icons.
- **Pricing Card**: A double-height (lg:row-span-2) yellow card featuring a vertical color-coded "PALS" header and large pixel-font price display.
- **Floating Icons**: Large, low-opacity (10%) Lucide icons (wifi, alert, gamepad, etc.) that float independently in the background.

## Page Sections
### Navigation
Fixed header with a white-translucent background. Features an SVG logo with "BUG" in blue and "ZERO" in lime. Navigation items use VT323 font at 21px (text-xl).

### Hero Section
Split layout. Left side contains a rotated badge, a large pixel-font heading with a gradient-text "ZÉRO", and a short description. Right side features a floating "Tablet" graphic—a red-bordered card tilted 3 degrees containing a "Bug Detected" warning. A dashed, rotating circle serves as a background element.

### Services Section (NOS_EXPERTISES)
A grit of cards. The standout is the yellow Pricing card ($80/hr). Other services are represented by color-blocked cards with specific icons: Computer (Neutral), Phone (Red), Gaming (Purple), Wi-Fi (Green), Home (Blue), and Server (Pink).

### About Section (POURQUOI_BUGZERO)
Uses a 12-column grid. Left side (4 cols) contains a sticky title and a thick 8px black underline. Right side (8 cols) contains white card blocks explaining the process, testimonials, and core values using bulleted lists with square markers.

### Contact Section
Centered call-to-action with three large, color-coded buttons (Red for Phone, Blue for Email, Pink for Instagram). Each button uses a layered "offset" shadow effect that expands on hover.

### Footer
Simple three-column layout on desktop containing the logo, contact details with hover color transitions (Red, Blue, Pink), and a copyright notice.

## Motion & Interaction
- **Float Animation**: Background icons and the hero tablet use a `float` keyframe (translateY -20px) with varying speeds (6s to 12s).
- **Spin Animation**: A background dashed circle rotates infinitely at a slow pace (20s).
- **Hard Shadow Hover**: Elements lift (translate -2px) and shadow deepens on hover.
- **Hard Shadow Active**: Elements sink (translate 4px) and shadow resets to 0 on click.
- **Glitch Feel**: The hero card uses horizontal white semi-transparent bars to simulate scan lines.

## Do's and Don'ts
- **Do**: Use high-contrast borders (2px black) on all interactive elements.
- **Do**: Maintain the 4px black hard shadow on all cards.
- **Do**: Use the VT323 font for all uppercase emphasis and UI labels.
- **Don't**: Use standard rounded corners or soft box-shadows.
- **Don't**: Use smooth transitions for position changes; prefer the "steppy" feel of the hard shadow translation.

## Accessibility
- **Contrast**: High contrast between text (Neutral-900) and backgrounds (White/Yellow).
- **Roles**: SVG logo includes `role="img"` and `aria-label="BugZero"`.
- **Interactivity**: Focus states are implied through the hard shadow active/hover logic, though standard focus rings should be preserved.

## Assets
1. Lucide Icons: `https://unpkg.com/lucide@latest`
2. Tailwind CSS: `https://cdn.tailwindcss.com`
3. Fonts: `https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=VT323&display=swap`
4. Logo/Icons: Inline SVGs and Lucide data-attributes (wifi, triangle-alert, gamepad-2, database, globe, cpu, menu, laptop, smartphone, home, server, phone, mail, instagram).
5. Background: CSS-generated 40px linear-gradient grid.

### Exported Codebase Asset Inventory
1. embed: https://fonts.gstatic.com
   Context: index.html: markup attribute; index.html: absolute url literal
2. embed: https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;family=VT323&amp;display=swap
   Context: index.html: markup attribute; index.html: absolute url literal
3. other: http://www.w3.org/2000/svg
   Context: index.html: absolute url literal
