# Cilantro Mexican Grill — Award-Winning Website Project
### Moneta, VA | Family-Owned Since Valentine's Day 2023 | Best Mexican by the Lake

**Live Repo:** https://github.com/eraykadirdemir/cilantro-web
**Business:** 1035 Mercantile St, Suite 102, Moneta, VA 24121 (Near Moneta Library) | Tiny strip mall, big flavors - parking tight on busy nights but worth it!
**Phone:** +1 540-297-3616 | **Email:** Cilantro.sml@google.com
**Hours:** Closed Mondays (Family rests) | Tue-Thu/Sun 11:30 AM - 9:00 PM | Fri-Sat 11:30 AM - 10:00 PM | Happy Hour 4-7pm

---

## About

Cilantro Mexican Grill opened **February 14, 2023 - Valentine's Day** in Moneta, VA. It's a fitting day for a place where love goes in all they do.

Family-owned by **Jose and Irma Perez and daughter Andrea Perez**, originally from Chesapeake, moved to Smith Mountain Lake 5 years before opening. Mom Irma named the restaurant and designed the menu. Daughter Andrea started helping young and worked way up to owner/manager. Staff of **12 employees who are like family** - reflected in everything.

Contemporary approach with **subtle green hints** that spice cilantro is known for, **hardwood floors, cozy fireplace, tasteful decorations**, bright clean light airy classy, home away from home, **no tacky murals** - refreshing per Yelp review.

**Signature Differentiators (Must be Hero):**
- **Tableside Fresh Guacamole** made to order + warm homemade tortilla chips + ranch dip
- **California Burrito** shrimp/chicken/steak/avocado/rice/spices/cheese dip show-stopper "best tasting dish I ever had"
- **Pina Rellena** grilled steak chicken pineapple tomatoes onions bell peppers melted cheese in half pineapple rice pico sour cream salad
- **Molcajete** large black volcanic pot overflowing grilled chicken ribeye steak shrimp pork chop sausage cactus (yes cactus!) onions two jalapeno stuffed peppers rice beans sour cream salad tortillas - conversational piece tastes as good as looks
- **Black Raspberry Margarita** frozen house simple refreshing beautifully balanced - drinks HUGE generous strong no shortcuts - margarita menu fairly large

**Rating:** Yelp 4.5 (36), Google 4.6 (225+ reviews) via Checkle, Facebook 86% recommend (18), Health Score 98/100, Roadtrippers 4.5 (36) - **Highest rated Mexican in Moneta area** vs Cancun 4.1 El Toreno 3.9 Mexico Viejo 2.8.

**Accessibility:** Wheelchair accessible entrance parking restroom seating per Zmenu, Outdoor seating patio + beautiful bar, Pets Allowed per Roadtrippers, WiFi Yes, Family Friendly Kids Friendly, Bar Seating, Takeout Yes Catering Yes Delivery No per Zmenu.

---

## Brand Stack - Single Source of Truth

All docs are enterprise-grade, fact-classified ✅ Verified Fact / 💡 Recommendation / ⚠ Assumption, no fabrication.

| Doc | File | Purpose |
|-----|------|---------|
| 01 SSOT | `knowledge/Cilantro-Mexican-Grill-SSOT.md` | 20+ sources, 19 sections, facts |
| 02 Brand Bible | `knowledge/Cilantro-Brand-Bible.md` | Essence Family Love Freshly Made, Mission, Archetype Caregiver 70% Creator 30%, Positioning |
| 03 Visual Identity Bible | `knowledge/Cilantro-Visual-Identity-Bible.md` | 21 parts - Logo, Color #2E7D32 #FFFBF2 #D87C45 #8E2F5B #F4C542, Typography Poppins/Inter, Tokens |
| 04 Art Direction Bible | `knowledge/Cilantro-Art-Direction-Bible.md` | Photography Canon EOS R5 50mm, Video, AI prompts |
| 05 Website Bible | `knowledge/Cilantro-Website-Bible.md` | IA + Sitemap mermaid + User Journey mermaid + Page Specs + SEO + WCAG + Performance + Analytics + Components |
| 06 UI Design System | `knowledge/Cilantro-UI-Design-System.md` | 19 components Button Badge Card Navbar Footer Hero Menu Accordion Alert Input Modal Map etc + tokens.css |
| 07 Master Prompt | `prompts/Cilantro-Award-Winning-Website-Prompt.md` | 31KB mega prompt for Lovable/Bolt/v0 to generate Awwwards site |

**SSOT Source Hierarchy:** SSOT > Brand Bible > Visual Bible > Art Bible > Website Bible > UI System. If conflict SSOT wins.

---

## Tech Stack - Award-Winning Target

**Stack:** Next.js 14 App Router TypeScript, Tailwind CSS, Poppins + Inter via next/font display swap, next/image WebP/AVIF responsive srcset, Framer Motion for motion 150-400ms expo, Lucide icons 2px stroke rounded, GA4 GTM, Vercel hosting, Cloudflare CDN.

**Performance Budgets:** LCP <2.5s (target 1.8s), CLS <0.1, INP <200ms, Total <2MB Home <1.5MB Menu, Images <150KB WebP each, JS <150KB gz, Lighthouse >=90 Performance Accessibility Best Practices SEO.

**SEO:** Title "Cilantro Mexican Grill | Best Mexican in Moneta VA & Smith Mountain Lake - Family Owned Since Valentine's Day 2023", Description includes address near Moneta Library phone rating Monday Closed Happy Hour, Canonical, OG 1200x630, Schema Restaurant LocalBusiness PostalAddress AggregateRating 4.6 OpeningHoursSpecification Menu MenuSection MenuItem FAQPage BreadcrumbList ImageObject, sitemap.xml robots.txt, GSC GBP Insights.

**Accessibility:** WCAG 2.1 AA+ - Charcoal #1A1A1A on Cream #FFFBF2 16.5:1 AAA, Green #2E7D32 on Cream 5.2:1 AA passes, focus visible 2px green + offset, keyboard nav skip link, touch target 44px min 48px rec, reduced motion media query.

**Design Tokens:** See `ui/tokens.css` + `ui/tokens.json`
```css
--color-primary: #2E7D32; /* Cilantro leaf subtle hints */
--color-bg-cream: #FFFBF2; /* Bright clean background dominant 60% */
--color-secondary: #D87C45; /* Terracotta fireplace */
--color-accent-berry: #8E2F5B; /* Black Raspberry Margarita */
--color-accent-yellow: #F4C542; /* Pineapple Pina Rellena */
--font-heading: 'Poppins'; --font-body: 'Inter';
--radius-md: 12px; --radius-lg: 16px;
--shadow-md: 0 4px 20px rgba(0,0,0,0.08);
--duration-base: 250ms; --ease-out-expo: cubic-bezier(0.16,1,0.3,1);
```

---

## Repo Structure (Fixed)

**Current Problem:** `knowledge/knowledge/` double nesting from upload - must flatten.

**Ideal Fixed Structure:**
```
cilantro-web/
- README.md (this file)
- .gitignore
- package.json
- app/ (Next.js scaffold from prompt)
  - globals.css (tokens.css)
  - page.tsx (Home)
  - layout.tsx
- knowledge/ (single level)
  - Cilantro-Mexican-Grill-SSOT.md
  - Cilantro-Brand-Bible.md
  - Cilantro-Visual-Identity-Bible.md
  - Cilantro-Art-Direction-Bible.md
  - Cilantro-Website-Bible.md
  - Cilantro-UI-Design-System.md
- ui/
  - tokens.css
  - tokens.json
- prompts/
  - Cilantro-Award-Winning-Website-Prompt.md (31KB master)
  - V0-Short-Prompt.txt (8KB for v0 token limit)
- docs/ (mirror for builders preferring docs/)
- public/
  - images/ (Yelp 34 + eventual pro shoot)
```

**Fix Commands:**
```bash
git mv knowledge/knowledge/* knowledge/
rmdir knowledge/knowledge
mv README-FIXED.md README.md
git add -A
git commit -m "fix: flatten knowledge folder, add proper README, tokens, prompts"
git push
```

---

## How to Use Award-Winning Prompt

### Option A: Lovable / Bolt.new / Framer AI (Recommended)

1. Copy entire file `prompts/Cilantro-Award-Winning-Website-Prompt.md` (MEGA PROMPT START)
2. Paste into Lovable prompt box
3. Attach folder `knowledge/` as Knowledge Base / RAG context (if builder supports)
4. Stack select: Next.js + Tailwind
5. Generate → Review Home hero Molcajete video + Trust Bar + Monday Closed badge red berry prominent + Near Moneta Library + Parking note + Signature 3 cards

### Option B: v0.dev (Token Limit)

Use `prompts/V0-Short-Prompt.txt` (8KB) + attach `knowledge/` files. v0 limit 10k chars - short version designed.

### Option C: Cursor / Claude Artifacts

Open repo in Cursor, open prompt file, use @reference knowledge files.

**What Prompt Generates (Award-Winning Check):**
- Hero Molcajete black pot sizzle loop muted poster WebM <2MB + slight vignette for white CTA text legibility
- Trust Bar: Google 4.6 ★ 225+ | Yelp 4.5 | Health 98 | Family-Owned Since Valentine 2023 | Outdoor Patio + Beautiful Bar | Wheelchair Accessible
- Signature 3 Cards: CA Burrito cross-section avocado layers, Pina Rellena pineapple boat, Molcajete black pot overflowing cactus
- Fresh Theater 50/50 video tableside guac molcajete bowl warm chips
- Story Teaser: Jose Irma Andrea photo Smith Mountain Eagle quote Contemporary Classic Delicious
- Menu Preview sticky pills categories + search + vegetarian filter 8+ dishes + Popular pineapple yellow badge + accordion Appetizers Soups Salads Nachos Enchiladas 8 styles Make-your-own-combo 2-3 items 24 sides Desserts fried ice cream churros Beverages Black Raspberry Margarita + call sticky bottom mobile
- Visit Split 50/50 Hours table Mon Closed red berry badge "Closed Mondays - Our family rests so we can serve yours better Tue-Sun" + Happy Hour 4-7pm + Summer Break June29-July6 + Address copy button + Coordinates 37.179379 -79.621713 + Map embed Place ID ChIJc4TWEQxHTYgRUWyKgtN78F8 + Landmark Near Moneta Library + Parking tiny strip mall tight worth it
- Gallery Masonry lightbox 34 Yelp photos alt descriptive
- Catering form large groups well
- Footer dark volcanic #1A1A1A cream text NAP Hours Social Facebook link newsletter Valentine's anniversary
- Sticky Bottom Mobile dual CTA: Call (540) 297-3616 primary green + Get Directions secondary outline 48px height safe area
- SEO schema + OG + performance <2MB + WCAG AA + GA4 events click_to_call click_directions menu_category_expand

**Forbidden:** Sombrero skulls chili pepper overload dark cantina HDR neon pure red #FF0000 primary Mexican flag heavy - must be bright clean contemporary lake house Sweetgreen meets modern lake house.

---

## Setup - After Prompt Scaffolds

```bash
npm install
# Add .env.local
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your_key
NEXT_PUBLIC_GA4_ID=G-XXXX
NEXT_PUBLIC_PLACE_ID=ChIJc4TWEQxHTYgRUWyKgtN78F8

npm run dev # localhost:3000
npm run build # Lighthouse check >=90
npm run lint
```

**Deploy:** Vercel connect repo cilantro-web, env vars, domain cilantromoneta.com, then set Google Business Profile website → https://cilantromoneta.com , Yelp website same.

---

## Sitemap

Home / | About /about | Menu /menu#appetizers | Visit /visit | Gallery /gallery | Catering /catering | Contact /contact | FAQ /faq | Privacy /privacy | Terms /terms | 404

**Mermaid User Flow:**
Discovery (Search Mexican Moneta VA) → Google Business 4.6 → Clicks website → Home hero Molcajete video + trust bar → Checks hours Monday Closed? → Scrolls signature → Views menu vegetarian filter → Visit map near Moneta Library parking → Mobile sticky Call + Directions → Phone call/directions → Dine-In chips/salsa/ranch immediately tableside guac huge margarita → Review prompt UGC #BestMexicanByTheLake → Loyalty first restaurant next visit

---

## Trust Builders - Must Show Everywhere Possible

- Google 4.6 ★ 225+ reviews via Checkle Yelp 4.5 Health Score 98/100 via Yelp 86% FB recommend Family-Owned Since Valentine's Day 2023 Outdoor Patio + Beautiful Bar Wheelchair Accessible Takeout Yes Catering Yes Delivery No Tiny Strip Mall but Worth It!

---

## QA Checklists

See `knowledge/Cilantro-Website-Bible.md` Appendices for Pre-Launch, Accessibility, SEO, Performance checklists. All must pass before launch.

**Quality Gate:** No invented facts beyond SSOT. If not publicly verified write Not publicly verified. All hard facts cited.

---

## License

MIT - Fonts Poppins Inter OFL free. Images Yelp 34 placeholder until pro shoot permission.

**Brand Governance:** Owner Andrea Perez final approver. Fact classification required. Monday Closed prominent everywhere. Near Moneta Library landmark + parking note must mention.

---

**END README - This repo will become award-winning restaurant website - Awwwards Site of the Day candidate - bright clean contemporary family love freshly made.**

