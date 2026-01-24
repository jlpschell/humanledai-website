# PROJECT.md - Human Led AI Website Build

## Project Overview

**Goal:** Build a professional marketing website for Human Led AI that converts visitors into booked demo calls.

**Model Site:** https://www.bookedin.ai/  
**Our Domain:** humanledai.net

**Key Difference from Model:**  
BookedIn sells a SaaS platform. We sell a done-for-you service. Our site should feel like "hire us to solve your problem" not "sign up for our software."

---

## Tech Stack

| Tool | Purpose | Why This Choice |
|------|---------|-----------------|
| **Astro** | Static site framework | Fast, simple, great for marketing sites |
| **Tailwind CSS** | Styling | Easy to apply brand colors, responsive out of the box |
| **Remotion** (future) | Video generation | Create animated explainer videos for demo sections |
| **Framer Motion** | Animations | Smooth scroll effects, hover states, transitions |
| **Vercel or Netlify** | Hosting | Free tier, easy deploy, fast CDN |

### Why Astro over Next.js?
- This is a marketing site, not a web app
- No need for React complexity
- Faster build times, simpler mental model
- Can add React components where needed (like interactive pricing toggle)

---

## Site Structure

```
humanledai-site/
├── src/
│   ├── components/
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── Hero.astro
│   │   ├── ProblemSection.astro
│   │   ├── SolutionSection.astro
│   │   ├── HowItWorks.astro
│   │   ├── UseCases.astro
│   │   ├── Testimonials.astro
│   │   ├── Pricing.astro
│   │   ├── CTA.astro
│   │   ├── TryItButton.astro
│   │   └── VideoPlaceholder.astro
│   ├── layouts/
│   │   └── MainLayout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   └── privacy.astro
│   └── styles/
│       └── global.css
├── public/
│   ├── images/
│   └── favicon.svg
├── AGENT.md
├── PROJECT.md
├── SITE-CONTENT.md
├── tailwind.config.js
├── astro.config.mjs
└── package.json
```

---

## Build Phases

### Phase 1: Foundation (Do First)
1. Initialize Astro project with Tailwind
2. Set up color variables from AGENT.md
3. Create MainLayout with Header and Footer
4. Build Hero section with headline, subheadline, CTA buttons
5. Create text-based logo component

**Milestone:** Homepage loads with hero section and navigation

### Phase 2: Core Sections
1. Problem section (3 pain points)
2. Solution section (how we fix it)
3. How It Works (3-step process)
4. "Try It Yourself" CTA button (links to external GHL funnel)

**Milestone:** Full story from problem → solution → action

### Phase 3: Social Proof & Conversion
1. Testimonials section (start with Ryan's Epoxy Floors)
2. Use Cases section (voice agent, database reactivation, lead gen)
3. Pricing section with commitment toggle
4. Final CTA section

**Milestone:** Complete homepage ready for review

### Phase 4: Polish & Launch Prep
1. Mobile responsiveness check
2. Add Framer Motion animations
3. Video placeholder sections (for future Remotion content)
4. Privacy policy page
5. Favicon and meta tags
6. Deploy to Vercel/Netlify

**Milestone:** Site ready for soft launch

### Phase 5: Future Enhancements
1. Remotion video generation for demo sections
2. Blog/content section (if needed)
3. GHL calendar embed (when ready)
4. Analytics integration

---

## Color Configuration (Tailwind)

Add to `tailwind.config.js`:

```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: '#0a2540',
        action: '#2563eb',
        accent: '#38bdf8',
        'bg-alt': '#f8fafc',
        'text-muted': '#374151',
      },
    },
  },
}
```

---

## Component Guidelines

### Buttons
- **Primary CTA:** `bg-action text-white hover:bg-action/90` → "Book a Demo", "Get Started"
- **Secondary CTA:** `bg-accent text-primary hover:bg-accent/90` → "Try It Yourself", "Learn More"
- **Ghost:** `border border-primary text-primary hover:bg-primary hover:text-white`

### Typography
- **Headlines (H1):** `text-primary font-bold text-4xl md:text-5xl lg:text-6xl`
- **Subheadlines (H2):** `text-primary font-semibold text-2xl md:text-3xl`
- **Body:** `text-text-muted text-base md:text-lg`
- **Font Family:** Inter or system sans-serif

### Sections
- Alternate between `bg-white` and `bg-bg-alt` for visual separation
- Max content width: `max-w-6xl mx-auto`
- Section padding: `py-16 md:py-24 px-4`

---

## External Links (Placeholders)

| Button/Link | Destination | Status |
|-------------|-------------|--------|
| "Book a Demo" | GHL booking page | Jay to provide URL |
| "Try It Yourself" | GHL demo funnel | Jay to build, then provide URL |
| "Get Started" | GHL booking page or contact form | Jay to decide |

For now, use `#` as placeholder and add comment: `<!-- TODO: Replace with GHL link -->`

---

## Video Placeholder Strategy

BookedIn has embedded demo videos. Until we create Remotion videos:

1. Create a `VideoPlaceholder.astro` component
2. Style it to look like a video thumbnail with play button
3. On click: either show "Coming Soon" modal or link to YouTube (if Jay records something)
4. Design should match brand colors (primary background, accent play button)

Future: Replace with Remotion-generated animated explainers

---

## Development Commands

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

---

## Deployment

**Recommended:** Vercel (free tier)

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
```

Connect to GitHub repo for automatic deploys on push.

---

## Quality Checklist (Before Launch)

- [ ] All links work (no broken hrefs)
- [ ] Mobile responsive (test on phone)
- [ ] Colors match brand guide
- [ ] Copy matches SITE-CONTENT.md
- [ ] CTA buttons have correct links
- [ ] Page loads fast (< 3 seconds)
- [ ] Favicon displays correctly
- [ ] Meta title and description set
- [ ] Privacy policy page exists
- [ ] "Try It Yourself" button ready (even if to placeholder)

---

## Notes for Claude Code

When Jay asks you to work on this project:

1. **Read AGENT.md first** - Understand the brand and voice
2. **Follow this PROJECT.md** - Build in the order specified
3. **Check SITE-CONTENT.md** - Use the exact copy provided
4. **Explain in plain English** - Jay is learning, not a developer
5. **Step-by-step terminal commands** - Number each step clearly
6. **Test before declaring done** - Run dev server, check the result
