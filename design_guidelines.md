# SlideSpark AI - Design Guidelines

## Design Approach

**Reference-Based Approach** - Drawing inspiration from leading SaaS design tools:
- **Canva**: Template-forward design, approachable UI, clear content hierarchy
- **Linear**: Sharp typography, modern spacing, polished micro-interactions
- **Stripe**: Professional credibility, clear value communication, trust-building elements
- **Notion**: Content-first layouts, clean organization, intuitive navigation

**Core Principles**:
1. Professional credibility that justifies $9.99/month subscription
2. Frictionless creation flow - from idea to presentation in minutes
3. Template showcase as hero - visual demonstration of value
4. Clear feature differentiation between Free and Pro tiers

---

## Typography System

**Font Stack**: 
- Primary: Inter (via Google Fonts CDN) - UI, body text, navigation
- Headings: Cal Sans or Sora - Marketing pages, hero sections, feature headlines
- Monospace: JetBrains Mono - Code snippets, technical details

**Hierarchy**:
- Hero Headlines: 4xl-6xl, font-bold, tight leading (leading-tight)
- Section Headings: 2xl-3xl, font-semibold
- Feature Titles: xl-2xl, font-semibold
- Body Text: base-lg, font-normal, relaxed leading (leading-relaxed)
- UI Labels: sm-base, font-medium
- Captions/Meta: xs-sm, font-normal

---

## Layout System

**Spacing Primitives**: Tailwind units of 2, 3, 4, 6, 8, 12, 16, 20, 24
- Micro spacing (within components): 2, 3, 4
- Component padding: 6, 8
- Section spacing: 12, 16, 20, 24
- Page margins: 4, 6, 8

**Grid Structure**:
- Marketing pages: max-w-7xl container, px-6 lg:px-8
- Dashboard: max-w-6xl container, px-4 lg:px-6
- Editor: Full-width with fixed sidebar (w-64), content area flex-1
- Template grid: grid-cols-1 md:grid-cols-2 lg:grid-cols-3, gap-6

**Responsive Breakpoints**:
- Mobile-first base styles
- md: 768px (tablet)
- lg: 1024px (desktop)
- xl: 1280px (large desktop)

---

## Component Library

### Navigation

**Marketing Header** (Landing/Pricing):
- Fixed top navigation with backdrop-blur
- Logo left, navigation center (hidden on mobile), CTA buttons right
- Mobile: Hamburger menu with slide-in drawer
- Height: h-16 to h-20
- Items: Logo, "Features", "Templates", "Pricing", "Sign In", "Start Free" (button)

**Dashboard Header**:
- Logo left, project search bar center, user menu right
- Persistent across all authenticated pages
- Height: h-16
- Quick actions: "+ New Project" button prominently placed

### Authentication

**Login/Signup Modal**:
- Centered modal (max-w-md)
- Social login buttons (Google) with icons, stacked above divider
- Email/password form below
- Clean toggle between Login/Signup states
- Trust indicators: "Secure login" text with lock icon

### Dashboard

**Project Grid**:
- Card-based layout, grid-cols-1 md:grid-cols-2 lg:grid-cols-3
- Each card shows: Thumbnail preview, title, last edited date, slide count
- Hover state: Subtle shadow elevation, "Edit" and "Delete" actions appear
- Empty state: Large illustration, "Create your first presentation" CTA
- Cards have aspect ratio of 16:9 for preview thumbnails

**Sidebar Filters** (if multiple project types):
- Fixed left sidebar (w-48 to w-64)
- Filter by: All Projects, Recent, Archived
- Template type filters

### Project Creation Flow

**Step 1 - Input Method Selection**:
- Two large, equal-width cards side-by-side (md:grid-cols-2)
- Option A: "Start from Topic" - icon, description, "Continue" button
- Option B: "Upload Text" - icon, file upload area, "Continue" button
- Clear visual distinction between choices

**Step 2 - Content Input**:
- If Topic: Large textarea (min-h-32), placeholder with examples
- If Text: File upload dropzone OR paste area, file format indicators
- Character/word count display
- "Generate Presentation" primary button

**Step 3 - Template Selection**:
- Full-screen template gallery
- Large previews (aspect-ratio-16/9), 3 columns on desktop
- Template categories at top (filters)
- Each template card: Preview image, name, "Free" or "Pro" badge
- Selected state: border highlight, checkmark indicator
- "Apply Template" sticky bottom bar

### Editor Interface

**Layout Structure**:
- Left sidebar (w-64): Slide thumbnails, drag handles for reordering
- Main canvas (flex-1): Current slide preview, editable text overlays
- Right panel (w-80): AI image suggestions, slide settings
- Top toolbar: Export buttons, template switcher, save status

**Slide Thumbnail List**:
- Vertical list with small previews
- Current slide highlighted
- Add slide button at bottom
- Drag indicators on hover

**Main Canvas**:
- Centered slide preview with proper aspect ratio
- Click-to-edit text fields with inline editing
- Image placeholders with "Replace" button overlay on hover
- Zoom controls in bottom-right corner

**AI Image Panel**:
- 3 suggested images per slide, stacked vertically
- Image thumbnails (aspect-ratio-square), hover to preview larger
- "Insert" button on each
- Search bar to find different images
- Source attribution (Unsplash)

### Export Modal

**Export Options**:
- Large modal (max-w-2xl)
- Two prominent cards: "Download as PPTX" and "Download as PDF"
- Each shows file icon, format details, estimated file size
- Pro feature badge if on free tier
- Export progress indicator when processing

### Pricing Page

**Hero Section**:
- Headline: Value proposition, subheading with key benefits
- Two-column pricing cards (Free vs Pro) centered
- Cards elevated with shadow, Pro card highlighted with subtle border
- Feature comparison checkmarks below cards
- "Start Free" and "Go Pro" CTAs

**Feature Comparison Table**:
- Clean table with alternating row backgrounds
- Checkmarks for included features
- "Pro Only" badges in specific rows
- Mobile: Cards instead of table

### Marketing/Landing Page

**Hero Section** (100vh):
- Split layout: Left side has headline, subheading, CTA buttons ("Start Free", "Watch Demo")
- Right side: Large animated mockup showing template examples OR video demo
- Trust indicators below CTAs: "No credit card required", "3 presentations free"

**Template Showcase**:
- Full-width carousel or grid of template previews
- 6-8 templates visible, slides horizontally
- Each preview clickable to enlarge
- Section headline: "Professional Templates for Every Need"

**Features Section**:
- 3-column grid on desktop, stacked on mobile
- Each feature: Icon (from Heroicons), title, description
- Features: "AI-Powered Generation", "Smart Image Suggestions", "One-Click Export", "Modern Templates", "Simple Editor", "Team Collaboration" (future feature teaser)

**How It Works**:
- 3-step visual flow (horizontal on desktop, vertical on mobile)
- Step numbers in circles, connecting line between them
- Each step: Illustration/screenshot, title, description

**Social Proof**:
- Testimonial cards in 2-column grid
- Each: User avatar, quote, name, role, company
- Star ratings above quotes

**CTA Section**:
- Full-width section with gradient or subtle pattern background
- Centered content: Headline, subheading, "Start Creating Free" button
- Secondary text: Feature highlight or time-saving stat

**Footer**:
- 4-column layout: Product links, Resources, Company, Legal
- Newsletter signup form in separate row above
- Social icons, copyright text

---

## Images

**Hero Image**: Large mockup showing SlideSpark interface with beautiful presentation displayed - should showcase the editor and a polished template. Position on right side of hero, taking 50-60% width.

**Template Previews**: Throughout the site, use actual presentation slide examples showing diverse topics (business, education, pitch decks). Each template should be visually distinct.

**Feature Illustrations**: Modern, abstract illustrations for the "How It Works" section - showing AI generation, template selection, and export flow.

**Dashboard Empty State**: Friendly illustration of a person creating or brainstorming.

---

## Micro-Interactions & Polish

**Buttons**:
- Primary CTA: Larger padding (px-6 py-3), font-semibold, rounded-lg
- Secondary: Outline style with hover fill
- Icon buttons: Square (h-10 w-10), centered icon
- On image buttons: Backdrop-blur background (backdrop-blur-sm bg-white/10)

**Cards**:
- Subtle shadow by default (shadow-sm)
- Elevation on hover (shadow-lg), smooth transition
- Rounded corners (rounded-xl)

**Form Inputs**:
- Consistent height (h-11 to h-12)
- Border on all sides, focus ring on interaction
- Placeholder text styling with reduced opacity
- Labels above inputs (text-sm font-medium)

**Loading States**:
- Skeleton loaders for project cards
- Spinner for AI generation
- Progress bar for export process

**Animations**:
- Minimal, purposeful only
- Modal fade-in (200ms)
- Page transitions (150ms)
- Hover state changes (100ms)

---

## Accessibility Standards

- Minimum touch target size: 44x44px for all interactive elements
- Focus indicators visible on all interactive components
- Form labels always present and associated
- ARIA labels for icon-only buttons
- Semantic HTML throughout (nav, main, article, section)
- Skip to main content link
- Keyboard navigation support in editor and galleries