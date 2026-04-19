# Pinehurst Golf Trip Planner — CLAUDE.md

## Project Vision

A free, comprehensive website for golfers planning a trip to the Pinehurst area of North Carolina — covering the Village of Pinehurst, Southern Pines, Aberdeen, and surrounding communities. The site combines honest editorial content (course guides, FAQs, dining/lodging recommendations) with a golf-buddy voice that tells you what's actually worth your time and money.

### Why This Exists

- **Learning project.** The primary goal is to learn Claude Code, modern web development (Astro), SEO, traffic monitoring, and marketing fundamentals.
- **Portfolio piece.** Code quality, design quality, and content quality all matter. Cut corners on scope, not craftsmanship.
- **Fills a real gap.** Search "Pinehurst golf trip" and you get the resort's own site, the CVB tourism page, and scattered one-off articles. There's no dedicated, opinionated, independent planning resource for the broader area.
- **Not revenue-first.** Monetization (affiliate links, possible sponsorship) may come later but must not compromise the user experience or editorial honesty.

### Voice & Tone

Write like a golf buddy who's been to Pinehurst a few times and is helping a friend plan their first trip. Opinionated but not arrogant. Practical over promotional. Say which courses are skippable. Give real cost estimates. Don't fake first-person experience on courses you haven't played — instead frame it as "here's what the rankings and reviews say."

The site author has played: Pinehurst No. 2, No. 3, No. 5, The Cradle, Southern Pines, Pine Needles, and Tobacco Road. Write first-person for those. Research-voice for the rest.

---

## Tech Stack

| Layer | Choice | Rationale |
|-------|--------|-----------|
| Framework | **Astro** | Static-first, ships zero JS by default, excellent SEO, "islands" architecture for future interactive components |
| Styling | **Tailwind CSS** | Utility-first, fast iteration, consistent design tokens |
| Interactive (future) | **React** (via Astro islands) | Trip planner tool will need client-side state; React is well-documented for Claude Code |
| Hosting | **Netlify** (free tier) | Git-based deploys, free SSL, good Astro support, $0/month at low traffic |
| Content | **Markdown / MDX** | Content lives in the repo as .md files, easy to author and version |
| Domain | **TBD — must include "Pinehurst"** | .com preferred, short and memorable. Not everyone knows the area as "the Sandhills." Budget ~$12/year. |

---

## Site Structure

### Pages

```
/                        → Homepage (hero, value prop, quick links to main sections)
/courses                 → All courses on one page, organized by tier, sticky side nav
/guide                   → First-timer's guide (how to book resort vs. off-resort, logistics, tips)
/stay                    → Where to stay (resort, vacation rentals, hotels, budget options)
/eat                     → Where to eat (by vibe: post-round casual, nice dinner, breakfast)
/faq                     → Frequently asked questions (with FAQ schema markup)
/about                   → About the site and the author
```

### Design Principles

- **Single courses page.** All courses live on one page with a sticky left-side nav that scrolls to each course section on click. No separate pages for each course — keeps it scannable, keeps people on the page (good for SEO dwell time), and avoids thin pages.
- **Content-first layout.** Generous whitespace, no sidebar clutter, mobile-first responsive.
- **No stock-photo carousels, no popup modals, no "Book Now" pressure.**
- **Warm editorial aesthetic.** Longleaf pine greens, sand/warm neutrals, deep navy accents. Refined serif for headings, clean sans-serif for body.

---

## Course Tiers

Courses are organized into tiers on the /courses page. Each tier has a name, a brief intro explaining what unifies the courses in it, and then individual course sections.

### The Main Event
**Pinehurst No. 2**
The reason most people come. Donald Ross masterpiece, U.S. Open anchor site (2024, 2029, 2035, 2041, 2047). Crowned greens, iconic bunkering, walking with a caddie is the way to do it. Requires resort stay (minimum 2 nights). Book 12+ months out. $$$$ with a $250 premium on top of package rates. Green fees roughly $300-600 depending on season.

### The A-List
Courses that would be the centerpiece of a golf trip anywhere else. At Pinehurst they share the stage with No. 2.

- **Pinehurst No. 4** — Gil Hanse redesign, bold and modern, pot bunkers, excellent conditioning. Resort course.
- **Pinehurst No. 10** — Tom Doak design, opened 2024, the newest resort course. Grand in scale, different feel from the rest. $125 premium on top of package.
- **Pine Needles Lodge & Golf Club** — Donald Ross design, four-time U.S. Women's Open host. Pure layout, walkable. Off-resort, has its own lodging and packages.
- **Southern Pines Golf Club** — Recently restored Ross design, classic bunkering, great value relative to quality. Strong word-of-mouth reputation.
- **Mid Pines Inn & Golf Club** — Another Ross design, vintage feel, top 25-30 in North Carolina. Lodge stay available. Part of the Pine Needles family.
- **Tobacco Road Golf Club** — Mike Strantz design. Polarizing, dramatic, unlike anything you've played. Towering sandhills, blind shots, massive bunkers. Love-it-or-hate-it but everyone should play it once.

### Strong Plays
Excellent courses that round out a trip. You won't regret playing any of these.

- **Pinehurst No. 8** — Tom Fazio design, player-friendly with elevated tees and wide fairways. Consistently ranked in Golf Digest's Top 100 Public. Resort course.
- **Pinehurst No. 3** — Shortest resort course, but a great warmup for No. 2. Tiny elevated greens demand precision and sharpen your short game before tackling the crowned greens of No. 2. Donald Ross design.
- **The Cradle** — 9-hole short course designed by Gil Hanse. Holes range 60-130 yards. The most fun you can have with your buddies at Pinehurst. Walk-up play available (don't have to be a resort guest).

### Local Picks
Off-resort courses that are well-regarded and offer good value. These are the courses locals and repeat visitors know about.

- **Mid South Club** — Arnold Palmer design, part of the Talamore Resort family. Attractive setting with longleaf pines and lakes. Accessible via stay-and-play packages.
- **Talamore Golf Club** — Rees Jones design, consistently ranked among the top public courses in NC. Known for its stay-and-play packages and (formerly) its llama caddies.
- **Tot Hill Farm** — Mike Strantz design, about 45 minutes from Pinehurst. If you loved Tobacco Road, this is more Strantz creativity. Dramatic elevation changes. Worth the drive.

### Fill Your Card
If you're staying 4+ days and want to play as much as possible, these courses round out a longer trip.

- **Pinehurst No. 9** — Ranked ~35th in NC. Solid resort course, a step below No. 8.
- **Pinehurst No. 1** — Where it all started. Historic but modest. A nice walk through history.
- **Pinehurst No. 5** — Fun layout, good for a lighter round. Not the strongest resort offering but enjoyable.
- **Pinehurst No. 6** — Tom Fazio design, more rugged and undulating than the other resort courses. A few miles from the main clubhouse.
- **Pinehurst No. 7** — Rees Jones design, ranked around 50th in NC. Challenging back nine.
- **Legacy Golf Links** — Nicklaus Design, classic Sandhills feel, good value.
- **Longleaf Golf & Family Club** — Dan Maples design, described as the "most playable course in the Sandhills."
- **Hyland Golf Club** — Highest elevation in the area, sparkling water features, affordable.

### The 19th Hole
**Thistle Dhu Putting Course**
Free. 18 holes. No greens fees. Grab a putter, grab a drink, and walk up. Designed by Gil Hanse in front of the main clubhouse verandah. Inspired by the original 1916 Thistle Dhu — widely considered America's first miniature golf course. The name is a play on "this'll do." Don't skip it. It's the kind of thing that turns a good trip into a great story.

---

## SEO Strategy

### Target Keywords (Long-tail, intent-driven)

**High priority — build pages around these:**
- "pinehurst golf trip" / "planning a golf trip to pinehurst"
- "pinehurst golf trip cost" / "pinehurst golf trip budget"
- "best courses near pinehurst"
- "first time pinehurst golf trip"
- "pinehurst golf trip itinerary"

**Medium priority — address within content:**
- "pinehurst no 2 green fees" / "how much does pinehurst no 2 cost"
- "where to stay pinehurst golf trip"
- "pinehurst caddie tips" / "pinehurst caddie cost"
- "best time to golf pinehurst"
- "pinehurst golf trip restaurants"
- "pinehurst vs tobacco road"

### Technical SEO (Built into Astro)
- Static HTML = fast load times = good Core Web Vitals
- FAQ schema markup (JSON-LD) on /faq page
- Open Graph + Twitter Card meta tags on all pages
- Sitemap via @astrojs/sitemap
- Descriptive, keyword-rich URLs
- Internal linking between courses, guides, and other pages
- Alt text on all images
- Mobile-first responsive design
- Answer the question in the first paragraph (featured snippet optimization)

### Content Principles
- **Opinionated, not encyclopedic.** Rank courses. Say what's skippable. Have a point of view.
- **Practical over promotional.** Real costs, real logistics, real tradeoffs.
- **First-person where earned.** Only for courses the author has played. Research-voice for the rest.
- **Update regularly.** Prices change, courses close for renovation, restaurants come and go. Freshness matters for SEO.
- **Data-backed findings stated as findings, assumptions labeled as assumptions, unknowns stated as unknowns.**

---

## Phasing

### Phase 1 — Launch
- Homepage
- Courses page (all tiers, sticky nav)
- First-timer's guide (includes booking info for resort vs. off-resort)
- FAQ page (with schema markup)
- About page

### Phase 2 — Depth
- Where to stay
- Where to eat
- Expanded course descriptions with more detail
- Images / photography

### Phase 3 — Interactive (separate project)
- Trip planner tool (React island or standalone app)
- User selects trip length, budget tier, course priorities
- Generates a custom day-by-day itinerary
- No backend — all client-side logic
- No login, no paywall

---

## Monetization Guardrails (Future)

- **Affiliate links:** Acceptable for lodging and gear. Must be clearly disclosed. Must not compromise editorial honesty.
- **Sponsorship:** Open to a tasteful title sponsor or section sponsor. One placement, not banner ads.
- **No display ads.** This is a portfolio piece.
- **No paywall.** All content free.

---

## Claude Code Setup Notes

### For someone new to the terminal

1. **Install Node.js** — Download from nodejs.org (LTS version). Required for Astro and Claude Code.
2. **Install Claude Code** — Follow Anthropic's install instructions.
3. **Open your terminal** — Mac: Terminal app or iTerm. Windows: PowerShell or Windows Terminal.
4. **Create a project folder** — `mkdir pinehurst-golf && cd pinehurst-golf`
5. **Place this CLAUDE.md in the project root** — Claude Code reads it automatically for context.

### Key Commands
```bash
npm create astro@latest    # Scaffold the Astro project
npm run dev                # Start local dev server
npm run build              # Build for production
# Deploy via Git push to Netlify (configured once)
```

### Expected Project Structure
```
pinehurst-golf/
├── CLAUDE.md
├── src/
│   ├── pages/
│   │   ├── index.astro
│   │   ├── courses.astro
│   │   ├── guide.astro
│   │   ├── stay.astro          (Phase 2)
│   │   ├── eat.astro           (Phase 2)
│   │   ├── faq.astro
│   │   └── about.astro
│   ├── components/
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── CourseSection.astro
│   │   ├── CourseNav.astro     (sticky side nav)
│   │   ├── FAQItem.astro
│   │   └── SEO.astro
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── data/
│   │   └── courses.json
│   └── styles/
│       └── global.css
├── public/
├── astro.config.mjs
├── tailwind.config.mjs
└── package.json
```

---

## Working Principles

- Ship incrementally. Phase 1 can launch with 5 pages.
- Content quality > content quantity. One great page beats three thin ones.
- SEO is a long game. Publish, index, iterate.
- This is a learning project — take time to understand what Claude Code is doing, not just accept the output.
