# Second Harvest Food Bank of NW NC — Homepage Prototype

The redesigned homepage for [Second Harvest Food Bank of Northwest North Carolina](https://www.secondharvestnwnc.org), built as a single-page static site with adaptive persona detection, an interactive food finder map, and the Ali virtual concierge widget.

## Structure

```
index.html      Main page — all HTML, CSS, and JS in one file
images/         Extracted site photography (18 assets)
```

## Design System

Built on the SHFBNWNC Design System v7 token set:

- **Typography:** DM Sans (Google Fonts)
- **Palette:** Navy `#2A3881` · Cranberry `#9E2B3A` · Amber `#E8A84D` · Wheat `#F7F3ED` · Steel `#3D3D3A`
- **Surfaces:** Frosted glass with layered transparency
- **Motion:** `cubic-bezier(0.16, 1, 0.3, 1)` for entrances

## Sections

1. **Adaptive Hero** — six-slide carousel (Default, Neighbor, Donor, Volunteer, Student, Catering)
2. **Get Involved** — GIVE / DO action cards
3. **Meal Maker** — donation impact calculator
4. **Food Finder** — SVG map with location search
5. **Mission Story** — parallax card
6. **Programs** — five program cards with hover reveals
7. **Impact Stats** — animated counters
8. **Volunteer** — CTA with background image
9. **Final CTA** — full-bleed closing section
10. **Footer** — contact, links, legal
11. **Ali Chat Widget** — virtual concierge (requires API configuration)

## Deploy

Static HTML with one Netlify serverless function for the Ali chat widget. No build step required.

### Netlify (recommended)

1. Push the repo to GitHub
2. Connect the repo in [Netlify](https://app.netlify.com) → **Add new site → Import an existing project**
3. No build command needed — leave it blank, set publish directory to `/`
4. Add your Anthropic API key as an environment variable:
   - Go to **Site settings → Environment variables**
   - Add `ANTHROPIC_API_KEY` with your key value
5. Trigger a redeploy

The Ali chat widget routes through `/.netlify/functions/ali`, which proxies requests to the Claude API with the key stored server-side. The key never touches the browser.

### GitHub Pages (static only)

Works for everything except the Ali chat widget (no serverless function support).

```bash
git add .
git commit -m "Homepage prototype v46"
git push origin main
```

## Notes

- The Ali chat widget uses a Netlify serverless function (`netlify/functions/ali.js`) to proxy requests to the Claude API. The `ANTHROPIC_API_KEY` environment variable must be set in Netlify for Ali to function.
- Food Finder links to `foodfinder.secondharvestnwnc.org` (live).
- All photography is embedded as extracted JPEG/PNG files in `/images`.
