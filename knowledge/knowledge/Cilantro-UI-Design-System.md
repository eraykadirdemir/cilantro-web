# UI DESIGN SYSTEM
## Cilantro Mexican Grill | Moneta, VA
### Version 1.0 | July 29, 2026 | Enterprise Reusable System for Website, Apps, Print

**Source Hierarchy:** SSOT (Facts) > Brand Bible (Strategy) > Visual Identity Bible (Visual Rules) > Art Direction Bible (Photo/Video) > Website Bible (IA & Strategy) > **This UI Design System (Implementation)**

**Purpose:** Single implementation source for designers (Figma) and developers (Next.js + Tailwind) to build consistent UI without reinventing. Every component uses design tokens from Visual Bible.

---

## 1. Overview & Principles

**✅ Verified Brand Core:** Bright clean contemporary hardwood floors fireplace subtle green #2E7D32 no tacky murals family-owned Valentine's 2023 Jose/Irma/Andrea staff 12 like family best Mexican by lake 4.6 Google 225+ Health 98 tiny strip mall near Moneta Library parking tight Monday Closed.

**💡 Design Principles (from Visual Bible):**
1. **Clean is Premium:** White space = cleanliness = quality. Cream bg #FFFBF2 60% white surfaces 20% green primary 10% terracotta secondary 5% berry/yellow accent 5%.
2. **Rounded & Welcoming:** 12-16px radius all cards buttons inputs friendly family not sharp corporate.
3. **Tight-Ship Precision:** 8px grid spacing, 24px gutter, 12-col grid, no misalignment - reflects tight service.
4. **Food as Hero Color:** Color from real dishes (pineapple yellow, berry purple) not decoration.
5. **Material Honesty:** Wood grain oak, volcanic black stone molcajete texture, linen - not fake.
6. **Mobile-First Lake:** 60% tourists at rental house phone searching, bottom sticky Call + Directions 48px tap targets.

---

## 2. Design Tokens

### Token Philosophy: Single source Figma + CSS variables + Tailwind. Never hardcode hex in components.

#### Color Tokens - CSS

```css
/* tokens.css - Cilantro Mexican Grill */
:root {
  /* Primary - Cilantro Leaf Green - Verified subtle green hints */
  --color-primary: #2E7D32; /* Poppins bold CTA */
  --color-primary-hover: #1B5E20;
  --color-primary-light: #8FA98C; /* Avocado */
  --color-primary-10: rgba(46,125,50,0.10);
  --color-primary-20: rgba(46,125,50,0.20);

  /* Secondary - Terracotta Fireplace */
  --color-secondary: #D87C45;
  --color-secondary-hover: #C06A37;
  --color-secondary-10: rgba(216,124,69,0.10);

  /* Accent - Black Raspberry Margarita verified deep pink */
  --color-accent-berry: #8E2F5B;
  --color-accent-berry-light: #FDF2F8; /* Monday Closed alert bg */

  /* Accent - Pineapple Yellow - Pina Rellena pineapple boat verified */
  --color-accent-yellow: #F4C542;
  --color-accent-yellow-light: #FFF8E1;

  /* Neutrals - Cream Background - Bright clean verified */
  --color-bg-cream: #FFFBF2;
  --color-bg-white: #FFFFFF;
  --color-bg-warm: #F5E6D3; /* Stone */
  --color-text-primary: #1A1A1A; /* Charcoal */
  --color-text-secondary: rgba(26,26,26,0.80);
  --color-text-tertiary: rgba(26,26,26,0.60);
  --color-border: #E0E0E0;
  --color-border-strong: #BDBDBD;

  /* Status */
  --color-success: #1B5E20; /* deeper green */
  --color-warning: #F4C542;
  --color-error: #B42318;

  /* Volcanic Black - Molcajete black pot verified */
  --color-volcanic: #1A1A1A;
  --color-volcanic-light: #2B2B2B;
}
```

**Tailwind mapping:** `tailwind.config.js` extend colors: `primary: var(--color-primary)` etc.

#### Typography Tokens

```css
:root {
  --font-heading: 'Poppins', system-ui, -apple-system, sans-serif; /* Primary - geometric friendly rounded */
  --font-body: 'Inter', system-ui, sans-serif; /* Secondary - humanist readable */

  /* Scale 1.25 modular */
  --text-xs: 12px;
  --text-sm: 14px;
  --text-base: 16px;
  --text-md: 18px;
  --text-lg: 20px;
  --text-xl: 24px;
  --text-2xl: 28px;
  --text-3xl: 36px;
  --text-4xl: 48px;
  --text-display: clamp(36px, 5vw, 48px);

  --leading-tight: 1.1;
  --leading-snug: 1.2;
  --leading-normal: 1.6;
  --tracking-tight: -0.02em;
  --tracking-wide: 0.08em;
}
```

**Usage:** H1 display Poppins Bold 700 --text-display tight, Body Inter 16px 1.6, Menu description 14px 1.5 80% opacity.

#### Spacing Tokens (8px grid)

```css
:root {
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px; /* Card padding */
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px; /* Mobile section */
  --space-16: 64px;
  --space-20: 80px; /* Desktop section */
}
```

#### Radius Tokens - Friendly 12-16px verified family not sharp

```css
:root {
  --radius-sm: 8px; /* Tags vegetarian popular */
  --radius-md: 12px; /* Buttons inputs alerts */
  --radius-lg: 16px; /* Cards images containers - primary */
  --radius-xl: 24px; /* Hero */
  --radius-full: 9999px; /* Pills Open badge */
}
```

#### Shadow Tokens - Soft diffused not harsh - Clean premium

```css
:root {
  --shadow-xs: 0 1px 2px rgba(0,0,0,0.04);
  --shadow-sm: 0 2px 8px rgba(0,0,0,0.06);
  --shadow-md: 0 4px 20px rgba(0,0,0,0.08); /* Card default */
  --shadow-lg: 0 8px 30px rgba(0,0,0,0.12); /* Hover */
}
```

#### Motion Tokens - Quick courteous tight-ship

```css
:root {
  --duration-fast: 150ms;
  --duration-base: 250ms;
  --duration-slow: 400ms;
  --ease-out-expo: cubic-bezier(0.16,1,0.3,1);
  --ease-in-out: cubic-bezier(0.65,0,0.35,1);
  --ease-bounce: cubic-bezier(0.34,1.56,0.64,1); /* Friendly badge pop */
}
```

#### Blur & Z-Index

```css
:root {
  --blur-nav: 12px;
  --blur-modal: 20px;
  --z-nav: 100;
  --z-sticky-cta: 101; /* Bottom mobile call+directions */
  --z-modal: 1000;
  --z-toast: 1100;
}
```

#### Breakpoints (from Visual Bible)

- sm 640px, md 768px (mobile nav switch), lg 1024px, xl 1280px (max container), 2xl 1536px

---

## 3. Foundations

### Color Usage

**Hierarchy 60-20-10-5-5:**
- 60% Cream #FFFBF2 background
- 20% White surfaces + Charcoal text #1A1A1A 16.5:1 AAA
- 10% Primary Green #2E7D32 CTAs links active
- 5% Terracotta #D87C45 secondary hover
- 5% Berry #8E2F5B Yellow #F4C542 accents - drinks popular badges

**Do:** Green primary CTA only 10% area not overwhelming - subtle hints per verified. **Don't:** Use pure red #FF0000 primary Mexican flag heavy - forbidden.

### Typography Scale & Usage

- **H1 Hero:** Poppins Bold 700 --text-display tight --tracking-tight --leading-tight charcoal on cream - "Contemporary Mexican, Made with Family Love"
- **H2 Section:** Poppins Semibold 600 36/28 --leading-snug
- **H3 Dish Category:** Poppins Semibold 28/22 - e.g., Appetizers
- **H4 Dish Name:** Poppins Semibold 18px - e.g., Pina Rellena
- **Body:** Inter Regular 16px 1.6 max 65ch
- **Menu Description:** Inter 14px 1.5 80% charcoal
- **Caption Uppercase:** Inter 12px uppercase tracking-wide medium gray
- **Price:** Poppins Medium 16px tabular-nums right align

### Layout Grid

- 12-col desktop 24px gutter 48px margin max 1280px container
- 8-col tablet 20px gutter 24px margin
- 4-col mobile 16px gutter 16px margin
- Section vertical padding 80px desktop 48px mobile
- Card internal 24px --space-6

### White Space Philosophy

White space = cleanliness verified bright clean classy. Generous. Never crowd 24 sides list. Use --space-20 between sections.

---

## 4. Components - Enterprise Library

### A. Button

**Anatomy:** Label + optional Icon left/right + loading spinner

**Variants:**
- **Primary:** BG var(--color-primary) text cream, hover var(--color-primary-hover) lift 2px shadow md->lg, radius 12px, Poppins Medium 16px, padding 12px 20px, 48px min height touch.
- **Secondary:** Outline border 2px var(--color-primary) text primary, hover fill primary cream.
- **Tertiary:** Text only primary, hover primary-10 wash.
- **Ghost White:** For dark footer volcanic bg, text cream border cream 20%.
- **Destructive Berry:** BG berry for Monday Closed? For delete if needed.
- **Sizes:** sm 36px height 14px, md 48px 16px (default), lg 56px 18px hero.

**States:** normal / hover lift 2px shadow lg bg darken 8% 200ms expo / active translateY 1px scale 0.98 / disabled opacity 0.4 cursor not-allowed / focus 2px green ring +2px cream offset / loading spinner + disabled

**Responsive:** Mobile full-width inside sticky bottom CTA, Desktop inline auto.

**Accessibility:** role button, aria-disabled, keyboard Enter Space, focus visible, contrast green on cream 5.2:1 AA passes, 44px min target recommendation 48px, aria-label if icon-only.

**Code Example (React Tailwind):**
```tsx
<button className="btn btn--primary btn--md" style={{background: 'var(--color-primary)', color: 'var(--color-bg-cream)', borderRadius: 'var(--radius-md)', boxShadow: 'var(--shadow-md)', transition: 'all var(--duration-base) var(--ease-out-expo)'}}>
  Call Our Family (540) 297-3616
</button>
```

### B. Badge / Pill

**Variants:**
- **Popular:** BG var(--color-accent-yellow) text charcoal --radius-full pill 8px padding 4px 10px Poppins Medium 12px - e.g., California Burrito Popular
- **Vegetarian:** BG var(--color-primary-light) #8FA98C text charcoal 80% + icon leaf - for 8+ vegetarian dishes verified Fajitas Vegetarianas etc.
- **Open:** BG var(--color-primary) text cream dot pulse - Open Now
- **Closed Monday:** BG var(--color-accent-berry-light) #FDF2F8 border 1px var(--color-accent-berry) text charcoal icon alert - Must be prominent everywhere hours per Brand Bible rule.
- **Health:** BG cream border green text green "Health Score 98/100" with icon
- **Rating:** BG white border light gray "4.6 ★ 225+"

**Size:** sm 20px height 12px font, md 24px 12px.

### C. Card

**Types:**

1. **Dish Card (Menu):**
- Anatomy: Image 4:3 rounded lg 16px overflow hidden scale 1.03 hover, Content padding 24px, Header name Poppins Semibold 18px + Price right tabular + Badges row Popular Vegetarian, Description Inter 14px 80%, Footer? Add-ons.
- States: normal shadow md, hover shadow lg lift 4px 250ms.
- Responsive 1-col mobile full width, 3-col desktop signature.

2. **Signature Card (Home 3-up CA Burrito Pina Rellena Molcajete):**
- Larger image 16:9, Title bold, Highlight e.g., "Show-stopper" quote "best tasting dish I ever had" from review, CTA View.
- Visual: black pot molcajete overflowing cactus image hero.

3. **Review Card:**
- Stars, Quote "best Mexican by lake", Name + Source Yelp/Google, Verified.

4. **Hours Card (Visit):**
- Table hours with Monday Closed red badge prominent alert icon + copy "Closed Mondays - Our family rests so we can serve yours better Tue-Sun", Happy Hour 4-7pm banner terracotta, Holiday Summer Break June29-July6 example alert.

5. **Trust Card / Feature:**
- Icon 32px line 2px rounded, Title, Description.

**Code:** article semantic h3.

### D. Navbar

**Anatomy:** Logo horizontal left (CILANTRO bold + Mexican Grill light) + Nav links About Menu Visit Gallery Catering Contact + Hours badge Open Now / Closed Monday + CTA double Call primary green + Get Directions secondary outline.

**Behavior:**
- Desktop: Transparent blur 12px over hero -> on scroll cream solid shadow sm, backdrop-filter var(--blur-nav) 80% opacity cream, transition 250ms.
- Mobile: Hamburger 24px icon line 2px rounded, drawer slide right 300ms expo 80% width cream, focus trap, Esc close, links large 20px Poppins Medium, CTA stacked full width bottom.

**Accessibility:** nav landmark aria-label primary, skip link to main, hamburger aria-expanded, keyboard Tab.

### E. Footer

- Dark volcanic #1A1A1A bg cream text #FFFBF2, logo reverse white, 4-col desktop: Brand NAP standardized 1035 Mercantile St Suite 102 Moneta VA 24121 + (540) 297-3616 + Cilantro.sml@google.com, Hours table, Quick Links, Newsletter email capture Valentine's anniversary.
- Social Facebook link https://www.facebook.com/p/Cilantro-Mexican-Grill-100090622722713/
- Bottom copyright + Trust badges Health 98 etc.

### F. Hero

- Variants: Video hero Molcajete sizzle loop muted poster fallback image WebP, Image hero Pina Rellena pineapple boat, Interior fireplace hardwood.
- Height 80vh desktop 60vh mobile, media cover centered, overlay gradient slight vignette for text legibility white text.
- Content left or centered? Left for home with parking note "Tiny strip mall big flavors - parking tight busy nights but worth it!" microcopy leaf icon.
- CTA primary View Menu + secondary Get Directions near Moneta Library.
- Trust Bar below hero immediate not inside.

### G. Menu Item Row (Alternative to Card for list view)

- List item border bottom 1px var(--color-border), padding 16px 0, layout: Name left bold + Description below + Price right tabular + Badges.
- Popular: dot leader? Optional.

### H. Accordion (Category)

- Header button Poppins Semibold 20px + count e.g., Appetizers 11, Icon chevron rotate 180deg 250ms expo, Body content grid dishes.
- Keyboard Enter Space expands, Arrow up/down navigates categories, aria-expanded.
- State expanded border left 2px primary accent? Optional.

### I. Filter Pills

- Pills row scroll horizontal snap mobile, Vegetarian Popular Chef's Choice? Actually Chef's Choice from article? Use Popular.
- Active state BG primary text cream, inactive white border light gray text charcoal hover primary-10.

### J. Alert / Banner

- Monday Closed: BG var(--color-accent-berry-light) #FDF2F8 border 1px var(--color-accent-berry) #8E2F5B, Icon alert triangle, Title "Closed Mondays", Copy "Our family rests so we can serve yours better Tue-Sun", radius md 12px padding 16px.
- Parking: BG cream border terracotta icon car "Tiny strip mall, big flavors - parking tight busy nights but worth it! Near Moneta Library."
- Holiday Summer Break: BG cream border terracotta icon calendar "Summer Break June 29 - July 6 - Our little summer break! Come see us before we close" (verified FB tone).

### K. Input / Form

- Label Inter Medium 14px charcoal + required *, Input 48px height border 1px var(--color-border) radius md 12px padding 12px 16px bg white focus border 2px var(--color-primary) ring 2px cream offset shadow xs, error border var(--color-error) + message berry text family tone "Oops! Our family missed your email".
- Textarea same 100px min, Select same 48px chevron icon.
- Checkbox custom green check.
- Accessibility label htmlFor aria-describedby error aria-invalid.

### L. Modal / Lightbox (Gallery)

- Overlay volcanic 80% opacity, Content white rounded xl 24px shadow lg max 90vw 90vh, Close button top-right 44px circle white shadow, Prev Next arrows, Keyboard Esc close Arrow nav, Focus trap.
- Image alt descriptive from Yelp caption e.g., "Cilantro Mexican Grill - piña rellena - Moneta VA".

### M. Map Embed (Visit)

- Placeholder static map image WebP 640w with address overlay "1035 Mercantile St Suite 102 Near Moneta Library", Click to load iframe Google Maps Place ID ChIJc4TWEQxHTYgRUWyKgtN78F8 lazy intersection observer, iframe title "Google Map of Cilantro Mexican Grill".
- Alternative links: Open in Google Maps Apple Maps MapQuest.

### N. Sticky Bottom CTA Mobile

- Visible only <768px, fixed bottom z 101 above nav, height 72px bg white border top 1px border shadow lg, 2 buttons 50/50: Call primary green full height + Get Directions secondary outline, safe area padding bottom env(safe-area-inset-bottom), hidden when keyboard open maybe JS.

### O. Trust Bar

- Horizontal row icons + text: Google 4.6 225+ (verified via Checkle), Yelp 4.5, Health 98, Family Since Valentine 2023, Outdoor Patio + Beautiful Bar, Wheelchair Accessible.
- Mobile scroll snap hide scrollbar.

### P. Testimonial Carousel

- Card review carousel dots nav autoplay paused hover, quote large Poppins, stars yellow #F4C542? Actually star green? Use yellow for stars.

### Q. Breadcrumb

- Home > Menu > Appetizers, Poppins 14px secondary text, current charcoal medium, separator chevron, nav aria-label breadcrumb.

### R. FAQ Accordion

- Q Poppins Medium 18px + icon plus/minus, A Inter 16px 80%, Schema FAQPage.

### S. Toast / Notification

- Success catering submit "Thank you for being part of our family! We will see you guys soon! Call (540) 297-3616 if need earlier." BG white border green shadow lg bottom right desktop bottom full mobile.

---

## 5. Patterns

### Pattern: Menu Filtering

- Flow: User lands /menu -> see category pills sticky top 80px below nav blur -> search input filter dishes name description -> toggles Vegetarian (8+ dishes verified) Popular -> results empty state "No dishes but our guac is always fresh! Try our California Burrito" + CTA Clear filters.

### Pattern: Large Group & Catering Inquiry

- Form fields: Name, Email, Phone, Guests (select 8-12 large groups well etc), Date (date picker), Event Type (reunion wedding birthday corporate), Message, Dietary notes vegetarian?
- Submit -> Thank you page /catering/thank-you + GA4 event + email to Cilantro.sml@google.com verified.

### Pattern: Monday Closed Handling

- Every page shows hours in footer + if Monday today banner top red berry alert persistent: "Closed Mondays - Our family rests... See you Tue-Sun 11:30am". Logic JS date.

### Pattern: Parking & Findability

- Visit page shows exterior photo strip mall Suite 102 + text "Tiny strip mall near Moneta Library very close to Moneta library cute restaurant/bar" verified + map + extra "More parking around side".

---

## 6. Layout Templates

### Template: Home

- Sections order: Navbar transparent, Hero 80vh, Trust Bar 80px, Signature 3-col 80px padding, Fresh Theater 50/50 video + text, Story Teaser 50/50 image text, Menu Preview pills + 6 dishes, Reviews Carousel, Visit Split 50/50 Hours table + Map, Gallery Teaser masonry 6, Catering CTA band berry light, Footer dark.

### Template: Menu

- Header small hero cream h1, Filter bar sticky, Accordion categories, Bottom sticky call mobile.

### Template: Visit

- Header hours alert Monday Closed, Split left hours table + right map, Below parking interior photos, FAQ link.

---

## 7. Accessibility Details per Component

- All components meet WCAG AA: Contrast charcoal on cream 16.5:1, green on cream 5.2:1 (Button primary white on green 5.0:1 AA passes), berry on light berry bg 7.2:1 but check.
- Focus visible 2px green + 2px cream offset.
- Touch target 44px min 48px per Visual Bible recommendation for bottom CTA.
- Reduced motion: Disable lift/parallax if prefers-reduced-motion.

---

## 8. Motion per Component

- Button hover lift 2px 200ms expo.
- Card hover lift 4px shadow lg 250ms.
- Image hover scale 1.03 400ms overflow hidden.
- Accordion expand height auto 300ms expo + chevron rotate 180deg 250ms.
- Modal fade + scale 0.95->1 300ms expo.
- Trust bar fade up 400ms stagger 80ms scroll observer.
- Navbar blur 12px transition 250ms.

---

## 9. Implementation Notes

### Tech Stack Recommendation (from Website Bible)

- Next.js 14 App Router, Tailwind CSS, tokens.css CSS variables, next/image WebP AVIF, next/font Google Fonts Poppins Inter with display swap subset latin, Vercel hosting.
- Icons: Lucide React custom line 2px rounded StrokeWidth 2, corner radius 2px.
- State: useState for menu filter, accordion.
- Analytics: GA4 GTM events click_to_call etc.

### Token Sync Figma ↔ Code

- Figma Variables: Create collection "Cilantro" with color primitives + semantic tokens primary etc same hex. Publish to devs. Ensure Figma tokens match tokens.css.

### Asset Requirements

- Professional photo shoot: Molcajete black pot cactus sausage etc, Pina Rellena pineapple boat, California Burrito cross-section avocado layers, tableside guac molcajete bowl warm chips, Black Raspberry Margarita huge purple condensation, interior hardwood fireplace beautiful bar patio summer/winter, exterior strip mall signage Suite 102 near Moneta Library, staff Andrea Jose Irma team 12 family.

### Naming Convention

- BEM + Tailwind: `.btn--primary`, `.card--dish`, `.badge--popular`.
- React components PascalCase: `<Button variant="primary" size="md" fullWidth={isMobile}>`
- Tokens kebab `--color-primary`.

---

## 10. Tokens JSON (for Figma/Style Dictionary)

```json
{
  "color": {
    "primary": {"value": "#2E7D32", "type": "color", "description": "Cilantro leaf green subtle hints verified"},
    "bgCream": {"value": "#FFFBF2", "type": "color", "description": "Bright clean light airy background"},
    "secondary": {"value": "#D87C45", "type": "color", "description": "Terracotta fireplace"},
    "accentBerry": {"value": "#8E2F5B", "type": "color", "description": "Black Raspberry Margarita deep pink verified"},
    "accentYellow": {"value": "#F4C542", "type": "color", "description": "Pineapple Pina Rellena"},
    "textPrimary": {"value": "#1A1A1A", "type": "color"}
  },
  "radius": {
    "sm": {"value": "8px"},
    "md": {"value": "12px"},
    "lg": {"value": "16px"}
  },
  "shadow": {
    "md": {"value": "0 4px 20px rgba(0,0,0,0.08)"}
  }
}
```

---

## 11. Quality Checklist per Component

Before shipping component:

- [ ] Token used not hardcoded hex?
- [ ] Radius 12-16px friendly?
- [ ] Shadows soft not harsh?
- [ ] Monday Closed logic if hours?
- [ ] NAP standardized 1035 Mercantile St Suite 102 + phone tel?
- [ ] Near Moneta Library landmark included if location?
- [ ] Parking note tiny strip mall worth it if visit?
- [ ] Vegetarian badge avocado #8FA98C + icon + text?
- [ ] Popular badge pineapple yellow?
- [ ] Photography bright clean hardwood fireplace not dark cantina alt descriptive?
- [ ] Contrast AA?
- [ ] Touch 44px min 48px?
- [ ] Keyboard nav Tab Esc?
- [ ] Motion 150-400ms expo reduced motion media query?

---

## 12. Do's & Don'ts (Component Level)

**Do:** Use cream bg dominant, white cards rounded 16px shadow md, green primary CTAs only 10% area, show real photos generous portions, Monday Closed red berry alert prominent, near Moneta Library landmark, parking note, trust badges Health 98 4.6.

**Don't:** Invent menu items pricing not verified, claim delivery DoorDash/Uber for Moneta (no verified), hide Monday closed small print, use pure red #FF0000 primary, use sombrero icons, sharp 0 radius everywhere, harsh shadows, stretched logo, dark cantina visuals, HDR oversaturated, plastic food styling.

---

**END OF UI DESIGN SYSTEM - Version 1.0 - This system must be used for all website, app, print, environmental builds. Tokens CSS + JSON are source.**

