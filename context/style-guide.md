# South Shore Analytics Style Guide

## Brand Identity

### Company Voice
- **Professional yet Approachable:** We're experts, but we explain things clearly
- **Data-Driven:** Everything we recommend is backed by evidence
- **Trustworthy:** 10+ years of experience, transparent pricing
- **Empowering:** We help you understand your data, not gatekeep it

### Key Messages
1. "Navigate your data journey with confidence"
2. "Analytics expertise at prices that make sense"
3. "Your guide through the complexities of modern data"

---

## Visual Identity

### Color Palette (Draft - To Be Refined)

**Primary Colors:**
```css
/* Nautical Blue (Lighthouse Theme) */
--primary-blue: #0A4B78;          /* Deep ocean blue */
--primary-blue-light: #1E6BA4;    /* Lighthouse beam blue */
--primary-blue-dark: #063552;     /* Night sea */

/* Accent Colors */
--accent-gold: #F4A623;           /* Lighthouse light / warning light */
--accent-teal: #2D9DA8;           /* Safe harbor / success */
```

**Neutral Palette:**
```css
--white: #FFFFFF;
--gray-50: #F9FAFB;
--gray-100: #F3F4F6;
--gray-200: #E5E7EB;
--gray-300: #D1D5DB;
--gray-400: #9CA3AF;
--gray-500: #6B7280;
--gray-600: #4B5563;
--gray-700: #374151;
--gray-800: #1F2937;
--gray-900: #111827;
--black: #000000;
```

**Semantic Colors:**
```css
--success: #10B981;    /* Green - safe passage */
--warning: #F59E0B;    /* Amber - caution */
--error: #EF4444;      /* Red - danger */
--info: #3B82F6;       /* Blue - information */
```

### Typography

**Primary Font:** Inter (Google Fonts)
- Clean, modern, excellent readability
- Variable font for performance
- Wide range of weights available

**Font Scale:**
```css
--font-display: 56px;      /* Hero headlines */
--font-h1: 40px;           /* Page titles */
--font-h2: 32px;           /* Section headers */
--font-h3: 24px;           /* Subsections */
--font-h4: 20px;           /* Card titles */
--font-body-lg: 18px;      /* Large body text */
--font-body: 16px;         /* Default body */
--font-body-sm: 14px;      /* Small text */
--font-caption: 12px;      /* Captions, labels */
```

**Font Weights:**
```css
--font-regular: 400;
--font-medium: 500;
--font-semibold: 600;
--font-bold: 700;
```

**Line Heights:**
```css
--leading-tight: 1.25;     /* Headlines */
--leading-normal: 1.5;     /* Body text */
--leading-relaxed: 1.75;   /* Long-form content */
```

### Spacing System

**Base Unit:** 8px
```css
--space-1: 4px;
--space-2: 8px;
--space-3: 12px;
--space-4: 16px;
--space-5: 20px;
--space-6: 24px;
--space-8: 32px;
--space-10: 40px;
--space-12: 48px;
--space-16: 64px;
--space-20: 80px;
--space-24: 96px;
```

### Border Radius
```css
--radius-sm: 6px;       /* Buttons, inputs */
--radius-md: 12px;      /* Cards */
--radius-lg: 16px;      /* Modals, large cards */
--radius-xl: 24px;      /* Hero sections */
--radius-full: 9999px;  /* Pills, avatars */
```

### Shadows
```css
--shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
--shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1);
--shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1);
--shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.1);
```

---

## Component Guidelines

### Buttons

**Primary Button** (Main CTAs)
- Background: `--primary-blue`
- Text: `--white`
- Hover: Lighten 10%
- Padding: 12px 24px
- Border radius: `--radius-sm`
- Font weight: `--font-semibold`

**Secondary Button** (Alternative actions)
- Background: transparent
- Border: 2px solid `--primary-blue`
- Text: `--primary-blue`
- Hover: Background `--primary-blue`, Text `--white`

**Ghost Button** (Tertiary actions)
- Background: transparent
- Text: `--gray-700`
- Hover: Background `--gray-100`

### Links
- Color: `--primary-blue`
- Hover: `--primary-blue-dark`
- Underline on hover
- Transition: 150ms ease

### Cards
- Background: `--white`
- Border: 1px solid `--gray-200`
- Border radius: `--radius-md`
- Shadow: `--shadow-sm`
- Padding: `--space-6`
- Hover: Lift with `--shadow-md`

### Forms
- Label: `--font-medium`, `--gray-700`
- Input height: 44px (accessible touch target)
- Border: 1px solid `--gray-300`
- Focus: 2px solid `--primary-blue`, remove default outline
- Error: Border `--error`, helper text `--error`
- Success: Border `--success`

---

## Animation Guidelines

**Timing:**
```css
--animation-fast: 150ms;     /* Micro-interactions (button hover, checkbox) */
--animation-normal: 300ms;   /* Standard transitions (dropdown, modal) */
--animation-slow: 600ms;     /* Page transitions, large movements */
--animation-hero: 2000ms;    /* Lighthouse beam rotation (one cycle) */
```

**Easing:**
```css
--ease-default: cubic-bezier(0.4, 0.0, 0.2, 1);  /* Standard easing */
--ease-in: cubic-bezier(0.4, 0.0, 1, 1);         /* Entering elements */
--ease-out: cubic-bezier(0.0, 0.0, 0.2, 1);      /* Exiting elements */
--ease-in-out: cubic-bezier(0.4, 0.0, 0.2, 1);   /* Smooth both ways */
--ease-bounce: cubic-bezier(0.68, -0.55, 0.265, 1.55); /* Playful bounce */
```

**Scroll Animation Principles:**
- Trigger animations at 20% viewport intersection (not 50% - feels more responsive)
- Use `transform` over `top/left` for better performance (GPU-accelerated)
- Fade + translate combinations: `opacity: 0 → 1` + `translateY(20px → 0)`
- Stagger child elements by 50-100ms for cascade effect
- Use CSS keyframes for simple animations (lighthouse beam, waves)
- Reserve JavaScript for interactive/complex animations only

**Principles:**
- Subtle and purposeful
- Never block user interaction
- Respect `prefers-reduced-motion` media query
- Enhance, don't distract
- Pause animations when off-screen (use IntersectionObserver for performance)

---

## Iconography

**Icon Library:** Heroicons (by Tailwind Labs)
- Consistent style with Tailwind
- Two variants: outline (default), solid (emphasis)
- Size: 20px or 24px default
- Color: Inherit from parent text color

---

## Responsive Breakpoints
```css
/* Mobile First Approach */
--screen-sm: 640px;    /* Small tablets */
--screen-md: 768px;    /* Tablets */
--screen-lg: 1024px;   /* Small laptops */
--screen-xl: 1280px;   /* Desktops */
--screen-2xl: 1536px;  /* Large desktops */
```

---

## Accessibility Standards

- **Color Contrast:** WCAG AA minimum (4.5:1 for body text, 3:1 for large text)
- **Focus States:** Always visible, 2px solid `--primary-blue`
- **Keyboard Navigation:** All interactive elements reachable via Tab
- **Screen Readers:** Semantic HTML, ARIA labels where needed
- **Motion:** Respect `prefers-reduced-motion` media query

---

## Writing Style

### Headlines
- Action-oriented when possible
- Benefit-driven (not feature-focused)
- Conversational but professional
- Example: "Turn Data Chaos into Clear Insights" not "Data Analysis Services"

### Body Copy
- Short paragraphs (2-3 sentences max)
- Active voice
- Second person ("you/your")
- Avoid jargon unless necessary (then explain it)

### CTAs
- Start with action verbs
- Create urgency without being pushy
- Be specific
- Examples:
  - "Get Your Free Data Assessment"
  - "See How We Can Help"
  - "Start Your Analytics Journey"

---

## Visual Metaphors

### Lighthouse Theme
- **Use for:** Hero section, navigation guidance, "we'll guide you" messaging
- **Visual elements:** Beam of light, waves, rocks, shoreline
- **Colors:** Nautical blues, golden light, teal water

### Data Journey
- **Use for:** Process explanations, case studies, capability overview
- **Visual elements:** Paths, milestones, progression charts
- **Avoid:** Overly complex diagrams (keep it simple)

---

## Do's and Don'ts

### ✅ Do:
- Use white space generously
- Lead with benefits, not features
- Show real work (case studies, examples)
- Make CTAs obvious and compelling
- Optimize for mobile first
- Use animations sparingly

### ❌ Don't:
- Use stock photos of people pointing at screens
- Overcomplicate the navigation
- Hide important info in modals
- Use more than 3 font weights
- Sacrifice performance for fancy animations
- Use technical jargon without context

---

## Image Guidelines

### Photography Style
- Authentic over staged
- Light and airy (not dark/moody)
- Focus on real work, real people
- Nautical/coastal themes where appropriate

### Illustrations
- Simple, clean line art
- Use brand colors
- Purposeful (not decorative only)
- SVG format for scalability

### Charts/Data Viz
- Use brand color palette
- Label clearly
- Accessible color combinations
- Animate on scroll (subtle)

---

## This is a living document
Update as design system evolves. Reference this guide for all design decisions.
```

---

### **4. .gitignore**

Open `.gitignore` and add:
```
# Dependencies
node_modules/
.pnp
.pnp.js

# Testing
coverage/

# Next.js
.next/
out/
build/
dist/

# Production
/build

# Misc
.DS_Store
*.pem

# Debug
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Local env files
.env
.env.local
.env.development.local
.env.test.local
.env.production.local

# Vercel
.vercel

# Backup
_backup/

# IDE
.vscode/
.idea/
*.swp
*.swo
*~