# Design Guidelines: ZenSpace Meditation App

## Design Approach
**Reference-Based Approach** inspired by premium meditation apps (Calm, Headspace, Insight Timer) with Material Design card components. The design prioritizes serenity, spaciousness, and gentle visual hierarchy to create a contemplative user experience.

## Core Design Principles
- **Breathing Room**: Generous whitespace creates mental clarity
- **Gentle Hierarchy**: Soft transitions between sections, nothing jarring
- **Centered Focus**: Content gravitates toward center alignment for meditation-appropriate grounding
- **Purposeful Motion**: Minimal, intentional animations only for breath guidance and state transitions

---

## Typography

**Font Families:**
- Primary: 'Playfair Display' (serif) - Headings, hero text, session titles
- Secondary: 'Inter' (sans-serif) - Body text, UI elements, metadata

**Type Scale:**
- Hero/Page Titles: text-5xl md:text-6xl, font-light
- Section Headers: text-3xl md:text-4xl, font-light
- Card Titles: text-xl md:text-2xl, font-normal
- Body Text: text-base, font-normal
- Metadata/Labels: text-sm, font-medium
- Micro Text: text-xs

**Letter Spacing:** Use tracking-wide for uppercase labels, tracking-normal for body

---

## Layout System

**Spacing Primitives:**
Core units: **2, 4, 8, 12, 16, 20** (as in p-2, m-4, gap-8, py-12, px-16, space-y-20)

**Container Widths:**
- Library Grid: max-w-7xl
- Player View: max-w-4xl
- Text Content: max-w-2xl
- Forms/Controls: max-w-md

**Section Padding:**
- Desktop: py-16 to py-20
- Mobile: py-8 to py-12
- Horizontal: px-4 md:px-8 lg:px-12

**Grid Patterns:**
- Session Cards: grid-cols-1 md:grid-cols-2 lg:grid-cols-3, gap-6
- Feature Displays: grid-cols-1 md:grid-cols-2, gap-8

---

## Component Library

### Navigation Header
- Sticky top navigation with backdrop-blur
- Logo centered or left-aligned
- Minimal menu items (Library, Custom, Profile)
- Search bar with rounded-full input, integrated icon
- Height: h-16 md:h-20

### Session Cards
- Rounded corners: rounded-2xl
- Padding: p-6
- Border: border border-opacity-20
- Shadow: shadow-sm hover:shadow-md transition
- Category badge: Small pill with category color, rounded-full px-3 py-1
- Layout: Icon/image top → Title → Duration/metadata → Description → CTA button

### Player Interface (Centerpiece)
- Full-screen or max-w-4xl centered layout
- Large circular breathing visualizer (min 300px, scales to viewport)
- Timer display prominent above visualizer (text-4xl md:text-5xl)
- Session title at top (text-2xl md:text-3xl)
- Controls below: Play/Pause centered, Stop/Back secondary
- Audio selector: Dropdown or segmented control below player
- Volume slider: Horizontal with icon, subtle styling

### Breathing Visualizer
- Circular SVG or div-based animation
- Smooth scale transforms (scale-100 to scale-150 for inhale)
- Glowing ring effect using box-shadow or radial gradients
- Phase text centered (text-xl md:text-2xl, uppercase, tracking-widest)
- Subtle pulsing during hold phases

### Buttons
- Primary: Rounded-full px-8 py-3, font-medium
- Secondary: Rounded-full px-6 py-2, border variant
- Icon Buttons: rounded-full p-3, size-12
- Hover states: Subtle scale-105 transform
- Focus: Ring offset for accessibility

### Form Controls
- Inputs: rounded-lg border, px-4 py-3
- Dropdowns: Custom styled select or listbox
- Sliders: Track height-2, thumb size-5, rounded-full
- Number steppers for breath timing: Inline +/- buttons

### Audio Controls Panel
- Horizontal layout: Volume slider + Sound selector
- Compact bar design, fixed or floating bottom
- Icons left-aligned, controls right
- Backdrop blur if overlaying content

---

## Images

**Hero Section:**
Large hero image on library landing page featuring serene nature scene (misty mountains, calm lake at dawn, meditation garden). Full-width, 60vh height on desktop, 40vh mobile. Subtle gradient overlay (from transparent to dark) for text legibility.

**Session Category Images:**
Each meditation card can include a small header image or icon representing its category (lotus for Vipassana, moon for Sleep, sunrise for Morning, etc.). These are accent images, not full card backgrounds.

**Player Background:**
Optional: Very subtle, blurred nature photograph as full-screen background during active session (low opacity, ~20%, to not distract).

**No images needed for:** Custom builder, search results, audio selector

---

## Animations

**Purposeful Only:**
- Breathing visualizer: 2-4s ease-in-out scale/opacity transitions matching breath rhythm
- Card hover: Subtle lift (translateY-1) + shadow increase, 200ms
- View transitions: 300ms fade-in opacity
- Play/pause button: Icon rotation or morph, 200ms

**Avoid:** Page scroll effects, excessive micro-interactions, parallax

---

## View-Specific Layouts

### Library View
- Hero section with search bar overlaying image
- Filter chips/tags below hero (horizontal scroll on mobile)
- 3-column grid of session cards
- Each card: 280-320px wide, auto height based on content
- Sticky header when scrolling

### Player View
- Centered single-column layout
- Session info header (title, category badge)
- Large breathing visualizer as focal point
- Timer above, controls below
- Audio panel at bottom or as sidebar on wide screens
- Exit/stop button top-left or top-right

### Custom Builder
- Form-based layout, max-w-md centered
- Grouped sections: Duration, Breath Pattern, Audio
- Clear labels, helpful microcopy
- Preview button launches into Player View
- Save to Library option (optional feature)

---

**Summary:** A tranquil, spacious design that prioritizes the meditation experience. Generous whitespace, soft shadows, centered layouts, and purposeful animation create a calming digital environment. Category colors add vibrancy without overwhelming. The breathing visualizer is the star—everything else supports it.