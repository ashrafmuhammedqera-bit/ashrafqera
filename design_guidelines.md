# Qera's Smart Assistant - Design Guidelines

## Design Approach

**Hybrid Strategy**: Combining the polished professionalism of Canva's user flow with Material Design's form components and the clean aesthetics of modern productivity tools like Notion and Resume.io.

**Core Philosophy**: Create a trustworthy, professional environment that makes CV creation feel effortless and confidence-inspiring. The design should feel both approachable and premium.

---

## Color Palette

### Light Mode
- **Primary Brand**: 217 91% 60% (Professional blue - trustworthy, corporate)
- **Primary Hover**: 217 91% 50%
- **Secondary Accent**: 142 76% 36% (Success green for completion states)
- **Background**: 0 0% 100% (Pure white)
- **Surface**: 220 14% 96% (Light gray for cards)
- **Text Primary**: 222 47% 11% (Near black)
- **Text Secondary**: 215 16% 47% (Muted gray)
- **Border**: 214 32% 91% (Subtle gray borders)

### Dark Mode
- **Primary Brand**: 217 91% 65%
- **Primary Hover**: 217 91% 55%
- **Secondary Accent**: 142 76% 41%
- **Background**: 222 47% 11%
- **Surface**: 217 33% 17%
- **Text Primary**: 210 40% 98%
- **Text Secondary**: 217 20% 70%
- **Border**: 217 33% 24%

---

## Typography

### Font Stack
- **Primary**: 'Inter', system-ui, -apple-system, sans-serif (Clean, modern, professional)
- **Headings**: 'Plus Jakarta Sans', sans-serif (Friendly yet professional for brand personality)

### Hierarchy
- **Hero/H1**: text-5xl md:text-6xl font-bold (Brand headlines)
- **Section Headers/H2**: text-3xl md:text-4xl font-bold
- **Card Headers/H3**: text-xl md:text-2xl font-semibold
- **Form Labels**: text-sm font-medium
- **Body Text**: text-base leading-relaxed
- **Helper Text**: text-sm text-secondary
- **Buttons**: text-sm md:text-base font-semibold

---

## Layout System

**Spacing Primitives**: Use Tailwind units of 2, 4, 6, 8, 12, 16, 20, 24 for consistent rhythm

### Container Strategy
- **Hero Section**: Full-width with max-w-7xl inner container, py-20 md:py-32
- **Content Sections**: max-w-7xl mx-auto px-4 sm:px-6 lg:px-8
- **Form Containers**: max-w-4xl for optimal reading and form completion
- **Template Gallery**: max-w-7xl for multi-column display

### Grid Patterns
- **Template Gallery**: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6
- **Feature Cards**: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8
- **Form Layout**: Single column on mobile, strategic 2-column splits on desktop for related fields

---

## Component Library

### Navigation
- **Header**: Sticky top navigation with logo left, primary CTA right
- **Style**: bg-white/80 dark:bg-surface/80 backdrop-blur-lg border-b
- **Height**: h-16 md:h-20
- **Logo**: Brand name "Qera's Smart Assistant" with subtle icon
- **CTA**: "Create Your CV" button prominent in primary color

### Hero Section
- **Layout**: Asymmetric 60/40 split (content left, visual right)
- **Content**: 
  - Headline: "Build Your Professional CV in Minutes"
  - Subheading: "Answer smart questions, choose your template, download your perfect CV"
  - Primary CTA: Large "Get Started Free" button
  - Trust indicators: "Join 10,000+ professionals" with small avatar stack
- **Visual**: Professional hero image showing diverse professionals or abstract CV template mockups
- **Background**: Subtle gradient from bg-surface to bg-white

### Multi-Step Form
- **Progress Indicator**: Horizontal step tracker at top showing: Personal Info → Experience → Education → Skills → Template → Preview
- **Active State**: Primary color with checkmarks for completed steps
- **Container**: Clean white/surface cards with rounded-2xl shadow-lg
- **Input Style**:
  - Labels: text-sm font-medium mb-2
  - Inputs: border-2 rounded-lg px-4 py-3 focus:ring-2 focus:ring-primary
  - Consistent height: h-12 for all inputs
  - Placeholder text in muted secondary color
- **Navigation**: "Back" and "Next" buttons at bottom, "Next" always primary colored
- **Validation**: Inline error messages in red with icon, success checkmarks in green

### Template Gallery
- **Layout**: Masonry-style grid with hover effects
- **Card Design**:
  - Template preview image/thumbnail
  - Template name overlay at bottom
  - Hover: Scale 105% with shadow-2xl
  - Selected state: ring-4 ring-primary
  - Quick preview button appears on hover
- **Categories**: Filter tabs above gallery (All, Professional, Creative, Modern, Classic)

### CV Preview Panel
- **Style**: Side-by-side view on desktop (form left, preview right in sticky panel)
- **Mobile**: Tab toggle between "Edit" and "Preview"
- **Preview Container**: Styled to look like paper with shadow-2xl
- **Zoom Controls**: Bottom right corner with +/- buttons

### Buttons
- **Primary**: bg-primary hover:bg-primary-hover text-white rounded-lg px-6 py-3 shadow-md
- **Secondary**: border-2 border-primary text-primary hover:bg-primary hover:text-white rounded-lg px-6 py-3
- **Outline on Images**: bg-white/20 backdrop-blur-md border-2 border-white text-white rounded-lg px-6 py-3 (no hover state implementation needed)
- **Icon Buttons**: rounded-full p-3 hover:bg-surface

### Cards
- **Standard**: bg-white dark:bg-surface rounded-2xl p-6 md:p-8 shadow-sm hover:shadow-lg transition-shadow
- **Featured**: ring-2 ring-primary/20 bg-gradient-to-br from-primary/5

---

## Page Structure

### Landing Page (Marketing)
1. **Hero**: Asymmetric layout with professional imagery, clear value proposition, prominent CTA
2. **How It Works**: 3-column grid showing steps (Question → Template → Download) with icons
3. **Template Showcase**: 6 template previews in 2-row grid
4. **Features**: 2-column feature highlights (Smart Questions, Multiple Formats, ATS-Friendly, etc.)
5. **Social Proof**: Testimonial cards in 3-column grid
6. **Final CTA**: Centered with gradient background
7. **Footer**: 3-column layout (Product, Company, Contact) with newsletter signup

### Application Flow
1. **Welcome Screen**: Brief intro, "Start Building" CTA
2. **Question Steps**: Progress bar → Form section → Navigation
3. **Template Selection**: Gallery with filters and preview modal
4. **Review & Edit**: Split view with CV preview
5. **Download**: Success state with download options (PDF/DOCX)

---

## Images

### Hero Section
- **Image**: Professional diverse group collaborating or close-up of polished CV document
- **Placement**: Right 40% of hero section
- **Style**: Subtle rounded corners (rounded-3xl), optional subtle shadow
- **Alt Approach**: Abstract geometric pattern in brand colors if photo unavailable

### Template Previews
- **Style**: Realistic CV document mockups showing actual template layouts
- **Aspect Ratio**: Portrait (standard CV dimensions)
- **Quality**: High-resolution, crisp text visible in thumbnail

### Feature Icons
- **Source**: Heroicons (outline style for consistency)
- **Size**: w-12 h-12 for feature sections
- **Color**: Primary brand color

---

## Animations & Interactions

**Philosophy**: Minimal, purposeful motion that enhances usability

- **Page Transitions**: Subtle fade-in for step changes (300ms)
- **Hover States**: Scale and shadow transforms (150ms)
- **Form Validation**: Smooth height transitions for error messages
- **Progress Steps**: Fill animation for completed steps
- **NO**: Excessive loading animations, flashy transitions, or distracting effects

---

## Key Differentiators

- **Professional Trust**: Clean, corporate-friendly design that doesn't feel overly playful
- **Guided Experience**: Clear visual hierarchy showing exactly what to do next
- **Template-First Thinking**: Templates are heroes, not afterthoughts
- **Responsive Form Design**: Mobile-optimized input experience with appropriate keyboards
- **Visual Progress**: Always show where users are in the process

This design creates a premium, professional CV-building experience that balances utility with visual appeal, ensuring candidates feel confident in their final CV output.