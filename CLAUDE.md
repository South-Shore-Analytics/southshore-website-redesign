# South Shore Analytics Website Redesign Project

## Project Mission
Transform South Shore Analytics' web presence from southshore.llc to southshoreanalytics.com with a modern, data-focused design that preserves SEO equity while elevating brand perception.

## Company Background
**South Shore Analytics** is a 10+ year analytics consulting firm founded by James Burke and Nick Lisauskas. We provide data analytics, integration, storage, visualization, and automated reporting services at competitive rates for businesses of all sizes.

**Core Differentiator:** Premium analytics expertise without premium-only pricing.

## Current State Analysis
- **Current Site:** https://www.southshore.llc/
- **Traffic Drivers:** Service area pages generate most inbound leads
- **Strengths:** Clear value proposition, established SEO presence
- **Weaknesses:** Outdated design, doesn't reflect modern analytics capabilities

## Project Goals (Priority Order)
1. **Modernize Design** - Inspired by minimal.gallery/tag/agency/ and sites in design-inspiration/
2. **Preserve SEO** - Keep service area pages, implement 301 redirects, maintain rankings
3. **Enhance Lead Gen** - Optimize conversion pathways without losing current lead flow
4. **Tell Our Story** - Use lighthouse visual metaphor to differentiate

## Key Design Concept: The Lighthouse
**Visual Metaphor for Hero Section:**
- **Lighthouse** = South Shore Analytics guiding you through data complexity
- **Rocky Waters** = Common data pitfalls (silos, quality issues, governance gaps)
- **The Journey** = Data maturity progression
- **Safe Harbor** = Data-driven business success

This should be an animated/interactive element that immediately communicates our value proposition visually.

## Design Inspiration Sources
See `design-inspiration/my-favorite-sites.md` for specific examples. Key themes:
- **operate.so** - Moving graphics, blueprint/technical aesthetic
- **adaline.ai** - Scroll-triggered animations
- **glyphicsoftware.com** - Process visualization, use case sections
- **vercel.com** - Clean minimal design with purpose
- **archetypeconsulting.com** - Animated hero section

## Technical Stack
- **Framework:** Next.js 14+ (App Router for SEO)
- **Styling:** Tailwind CSS (utility-first for rapid iteration)
- **Animations:** Framer Motion (for lighthouse interactions)
- **SEO:** Built-in Next.js SEO + structured data
- **Deployment:** Vercel (for performance)

## MCP Tools Available
- **Exa:** Research current site, analyze competitors, gather design inspiration
- **Playwright:** Automated design review, accessibility testing, responsive checks

## Design Standards
Refer to `context/design-principles.md` for comprehensive checklist. Key priorities:
- **Performance First:** 90+ Lighthouse score (fast load times critical for analytics firm)
- **Accessibility:** WCAG AA minimum (inclusive design)
- **Mobile Responsive:** Mobile-first approach
- **SEO Optimized:** Semantic HTML, structured data, meta tags
- **Minimal & Clean:** Lots of white space, clear hierarchy

## Development Workflow

### Phase 1: Research & Analysis
1. Use **Exa** to analyze https://www.southshore.llc/
2. Document strengths/weaknesses in `research/current-site-analysis.md`
3. Research inspiration sites for specific techniques
4. Create design system in `context/style-guide.md`

### Phase 2: Design Prototypes  
1. Create 3 homepage concepts in `prototypes/homepage-concepts/`
2. Use HTML/CSS/vanilla JS for rapid prototyping
3. Focus on lighthouse hero concept variations
4. Include mobile responsive breakpoints

### Phase 3: Design Review
1. Invoke `@design-review` agent for each prototype
2. Test with Playwright: interactions, responsiveness, accessibility
3. Document findings and iterate
4. Present final 3 concepts for stakeholder selection

### Phase 4: Development
(After design approval - not started yet)

## Communication Preferences
- **Present Options:** Show 2-3 alternatives with trade-offs
- **Explain Decisions:** Provide rationale for recommendations
- **Use Artifacts:** Create visual prototypes immediately
- **Ask Questions:** Clarify before building
- **Evidence-Based:** Screenshot issues, cite sources

## SEO Requirements (Critical)
- Map all current southshore.llc pages to new structure
- Create comprehensive 301 redirect file
- Preserve all service area pages (primary lead source)
- Implement structured data (LocalBusiness, Service, FAQPage)
- Optimize meta titles/descriptions
- Monitor Search Console during/after migration

## Success Criteria
- [ ] 3 compelling homepage prototypes created
- [ ] Lighthouse hero concept implemented with animation
- [ ] 90+ performance score on all prototypes
- [ ] WCAG AA accessibility compliance
- [ ] Comprehensive website roadmap document created
- [ ] SEO migration strategy documented
- [ ] Stakeholder approval on selected design

## Files to Reference
- **PRD:** See PRD.md for detailed requirements
- **Design Principles:** context/design-principles.md
- **Style Guide:** context/style-guide.md (to be created)
- **Inspiration:** design-inspiration/my-favorite-sites.md
- **Agent Config:** agents/design-review.md

## Questions for Clarification
When uncertain, ask about:
- Content availability (case studies, testimonials, images)
- Brand preferences (colors, tone, messaging)
- Technical constraints (hosting, budget)
- Timeline expectations

## Current Phase
**Phase 1: Research & Analysis** - Use Exa to analyze current site and create initial recommendations.