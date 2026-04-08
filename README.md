# Second Harvest Food Bank of Northwest NC — Homepage

Production homepage for [secondharvestnwnc.org](https://secondharvestnwnc.org), designed and built as part of the 2026 website redesign.

## Features

- **Rotating hero** — 5 persona variants (default, neighbor, volunteer, donor, student) cycle every 15s with Ken Burns + crossfade
- **Apple-style mega dropdowns** — 6 nav items with animated hover panels, featured cards, and dim overlay
- **Food Finder** — Interactive zip code search with Leaflet.js map and live results
- **Empty Bowls 2026** — Time-limited event section (auto-hides after April 22, 2026)
- **Ali chat widget** — Alimentum OS virtual concierge bubble
- **Floating CTAs** — "Need food?" and "Donate" pills appear on scroll
- **Mobile responsive** — Breakpoints at 900px and 600px with frosted hamburger menu

## Design System

| Token | Value | Role |
|-------|-------|------|
| Navy | `#2A3881` | Authority, navigation |
| Cranberry | `#9E2B3A` | Action, primary CTAs |
| Amber | `#E8A84D` | Reward, Meal Makers |
| Wheat | `#F7F3ED` | Page background |
| Cream | `#FDFCFA` | Card backgrounds |
| Wood | `#C9B99A` | Accents, borders |
| Slate | `#3D3D3A` | Body text |
| Forest Green | `#2D6A38` | Volunteer CTAs |

**Font:** DM Sans (300, 400, 500, 600) · **Border radius:** 12px (global), 50px (hero pills)

## Deployment

Static site — no build step required.

```bash
netlify deploy --prod --dir=.
```

## Team

- **Creative Direction & Development:** Matt Nooe
- **Organization:** Second Harvest Food Bank of Northwest North Carolina
