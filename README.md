# Andy Mandel — spec redesign

A speculative redesign of [soldbymandelteam.com](https://soldbymandelteam.com) for Andy Mandel, Founder & CEO of The Mandel Team | eXp Realty in Coral Springs. It keeps Andy's existing copy and gives it a South Florida deco design: sand, harbor ink and sunset coral, set in Cormorant Garamond and Jost.

![Desktop hero](preview/desktop-hero.jpg)

Static HTML, CSS and JS. No build step, no dependencies apart from Google Fonts.

## Preview locally

```bash
cd ~/dev/andy-mandel-spec && python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy

Import this repo in Vercel (Framework preset: **Other**, no build command, output directory: root). Every push to `main` redeploys.

Or from the CLI:

```bash
cd ~/dev/andy-mandel-spec && npx vercel --prod
```

The page ships with `<meta name="robots" content="noindex, nofollow">`, and `vercel.json` adds an `X-Robots-Tag: noindex` header, because it uses Andy's real name and branding. Remove both only if Andy signs and the site goes live.

## What's on the page

- Hero with a generated illustration in a stepped deco arch (slowly turning sunburst, palms, a modern villa on the water) and a "#1 in Coral Springs, RealTrends Verified 2025" badge.
- Count-up stats: 1,500+ homes sold, $113.0M 2025 volume, 163 transaction sides, licensed since 2013.
- "Three ways to sell": 7 Day Marketing Blitz, Instant Cash Offer (with eligibility rules) and Traditional Listing.
- A Blitz section built around a large "7" with the six components, and the flexible-commission statement in a deco frame.
- Meet Andy, areas grouped by county, reviews, and a home-value form (validated, not wired to a CRM).
- Footer with the Equal Housing Opportunity notice, RealTrends attribution and cash-offer terms note.

## Verify before pitching

The copy was gathered from Andy's live site through a search index, so check it against the site:

- **Reviews are condensed** from the testimonials on soldbymandelteam.com. Swap in the verbatim text and reviewer names (an HTML comment marks the spot).
- **Three phone numbers appear.** His site shows 954-751-4360 and 954-513-4204; RealTrends and LinkedIn show 954-610-0563. The spec uses 954-751-4360.
- **A list-price guarantee was left out.** One source described a written guarantee to pay the difference if a home doesn't sell at 100% of list price. It couldn't be confirmed; if it's real, it belongs in the hero.
- **Bio details come from third-party profiles** (FSU double major, born and raised in Parkland and Coral Springs, specialties, "16 agents plus support staff").
- **Placeholders:** the illustration and the "AM" portrait monogram stand in for a listing photo and Andy's headshot.
- **The home-value form isn't wired up.** Point it at the team's CRM or lead endpoint before launch.
