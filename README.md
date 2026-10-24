# NHY Artists

A complete, five-page boutique electronic music agency prototype. Art direction: 89th FLOOR. Built with HTML, CSS and vanilla JavaScript; no dependency installation or build step is required.

## Run locally

Requires Node.js 18 or newer.

```sh
npm start
```

Open http://127.0.0.1:4173. Set `PORT` if needed. `npm run check` checks JavaScript syntax. The `dist` directory can also be deployed to any static web host. All five routes are actual HTML files, so direct links and browser back/forward work without SPA fallback routing.

## Pages

- `dist/index.html` — agency introduction, sculptural hero, featured artists.
- `dist/artists.html` — searchable roster, genre filters, grid/list view, empty/reset state.
- `dist/artist.html?id=eli-voss` — individual artist. All six roster identities have their own content through this template.
- `dist/bookings.html` — four-step promoter enquiry: talent, event, contact, review; validation and text brief download.
- `dist/about.html` — Nick Yates, philosophy, contact routes and 89th FLOOR direction.

## Prototype boundaries

All six artist names, biographies, cities, dates and venues are illustrative fictional content. Press portraits are generated placeholders, not real represented artists. Nick Yates’s 20 years of experience and Paradise/Kaluki background come from the supplied brief.

No messages are sent and no booking is confirmed. The booking form creates a downloadable text brief. Contact details stay in page memory only and clear on page reload/navigation. Only the motion preference uses local storage. A confirmed agency email or form backend is needed before live enquiries can be routed. No invented email address is used.

The artist listening controls play 30-second procedural audio sketches, generated in-browser using Web Audio. They are clearly marked as demo audio, not artist recordings. Replace these with approved listening links/media before a public launch.

Type uses Google Fonts (DM Sans and Space Mono) with local Arial/monospace fallbacks. The portrait sheet is bundled locally. The site remains usable without Google Fonts.

## Future 3D integration

The prototype deliberately keeps booking controls independent of visual scenes. Explicit mounts in `dist/app.js`:

1. `[data-scene="hero-sculpture"]`: current lightweight animated SVG sculpture; replace or enhance with a Three.js canvas.
2. `[data-scene="artist-portal"]`: portrait containers with hover interaction, suitable for a pointer-reactive shader or depth portal.
3. `[data-scene="atmospheric-particles"]`: footer CTA band, reserved for a subtle decorative particle field.

Keep decorative canvases `aria-hidden` and `pointer-events: none`. Preserve portrait and SVG fallbacks. Respect `prefers-reduced-motion` and the `.no-motion` setting, stop rendering when offscreen, cap device pixel ratio, and avoid blocking page navigation or form rendering on 3D loading. No Three.js dependency is needed for this version.

## Content and visual changes

The `artists` array at the top of `dist/app.js` contains the fictional roster. Shared layout and interactions also live there. Design tokens and responsive rules are in `dist/styles.css`. The contact sheet uses CSS background positioning: three columns, two rows; each portrait is square.

See `ASSET-PROVENANCE.txt` for the generated image prompt and source. This is an editable concept, not a final production agency website.
