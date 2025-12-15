# Image Compression Tool - Design Guidelines

## Design Approach
**Hybrid Approach**: Drawing inspiration from modern utility tools like TinyPNG and Squoosh, combined with Material Design principles for clean, functional interfaces. Focus on clarity, trust-building, and immediate usability.

## Typography System
- **Primary Font**: Inter (Google Fonts) - clean, modern, excellent readability
- **Headings**: 
  - Hero H1: text-5xl md:text-6xl font-bold
  - Section H2: text-3xl md:text-4xl font-bold
  - Feature H3: text-xl font-semibold
- **Body Text**: text-base md:text-lg leading-relaxed
- **UI Labels**: text-sm font-medium uppercase tracking-wide

## Layout System
**Spacing Framework**: Use Tailwind units of 4, 6, 8, 12, 16, 20, and 24 for consistent rhythm
- Section padding: py-16 md:py-24
- Container max-width: max-w-6xl mx-auto px-6
- Component gaps: gap-8 or gap-12
- Card padding: p-6 or p-8

## Page Structure (7 Sections)

### 1. Header
Sticky navigation with:
- Logo/brand name (left)
- Primary navigation links: Features, How It Works, FAQ (center)
- "Get Started" CTA button (right)
- Trust indicator: "10,000+ Images Compressed Daily" badge

### 2. Hero Section (70vh)
**Layout**: Two-column split (lg:grid-cols-2)
- **Left Column**: 
  - Compelling headline emphasizing speed and quality
  - Supporting description (2-3 lines)
  - Key benefits bullets with checkmark icons (Heroicons)
  - Primary CTA button
  - Trust badges: "Free • No Sign Up • Secure"
- **Right Column**: 
  - Hero image showing before/after compression visualization
  - Overlaid stats card showing file size reduction example

### 3. Interactive Upload Section (60vh minimum)
Prominent drag-and-drop upload area:
- Large dashed border container with centered content
- Upload icon (heroicons/arrow-up-tray)
- "Drag & drop or click to upload" text
- Supported formats indicator
- File size limit notice
- Compression quality slider component (visible after upload)
- Before/after file size comparison cards (side-by-side)

### 4. Features Grid (3 Columns on Desktop)
Six feature cards in grid-cols-1 md:grid-cols-2 lg:grid-cols-3:
- Each card: Icon (top), title, 2-line description
- Features: Lossless Quality, Instant Processing, Batch Upload, Privacy First, Format Support, Free Forever
- Subtle card elevation with rounded-lg borders

### 5. How It Works (3-Step Process)
Horizontal timeline layout (grid-cols-1 md:grid-cols-3):
- Step indicators with large numbers
- Step title and detailed description
- Connecting lines between steps (hidden on mobile)
- Supporting icon for each step

### 6. Stats/Social Proof Section
Four-column stat display (grid-cols-2 lg:grid-cols-4):
- Large metric numbers (text-4xl font-bold)
- Descriptive labels below
- Metrics: Images Compressed, Data Saved, Average Compression %, Processing Speed

### 7. FAQ Section
Two-column layout on desktop (lg:grid-cols-2):
- 6-8 common questions
- Expandable accordion pattern
- Question as trigger, answer revealed below
- Icons for expand/collapse states

### 8. Footer
Three-column grid (grid-cols-1 md:grid-cols-3):
- **Column 1**: Brand logo, tagline, social media icons
- **Column 2**: Quick links (About, Privacy, Terms, Contact)
- **Column 3**: Newsletter signup form with email input and subscribe button
- Bottom row: Copyright and additional legal links

## Component Library

### Buttons
- **Primary**: Rounded-full, px-8 py-4, font-semibold, shadow-lg with blur backdrop when on images
- **Secondary**: Rounded-full, px-8 py-4, border-2, font-semibold
- **Icon buttons**: Square aspect-ratio, rounded-full, p-3

### Cards
- Rounded-xl borders with subtle shadow
- Padding: p-6 or p-8
- Hover state: slight scale transform (scale-105)

### Upload Zone
- Rounded-2xl with dashed border-2
- Min-height: min-h-96
- Transition states for drag-over highlighting
- Center-aligned content with flex column

### Progress Indicators
- Linear progress bar during compression
- Percentage text overlay
- Smooth animated fill transition

### Icons
**Library**: Heroicons (CDN)
- Upload: arrow-up-tray
- Check: check-circle
- Download: arrow-down-tray
- Image: photo
- Lightning: bolt
- Shield: shield-check

## Images Section
**Hero Image**: Right side of hero section - modern dashboard/interface mockup showing the compression tool in action with visible before/after comparison. Clean, professional screenshot or illustration demonstrating the interface. Image should be high-quality with subtle shadow and rounded corners.

**Supporting Graphics**: Consider abstract illustrations of file compression (visual metaphors like folders getting smaller) in the "How It Works" section.

## Animations
Minimal, purposeful animations only:
- Upload zone: Subtle pulse on hover
- Progress bar: Smooth width transition
- Stat counters: Count-up animation on scroll into view
- File drop: Scale and fade transition

## Accessibility
- High contrast text throughout
- Focus states on all interactive elements (ring-2 ring-offset-2)
- ARIA labels on icon-only buttons
- Semantic HTML structure with proper heading hierarchy
- Keyboard navigation support for upload and controls