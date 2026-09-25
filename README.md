# emmasampietro.github.io

My personal website — **[emmasampietro.github.io](https://emmasampietro.github.io)**

A single static page covering my education, research experience, and academic projects,
each linked to its code, report and figures.

## Built with

Plain HTML, CSS and a little vanilla JavaScript. No framework, no build step, no
dependencies — what is in this repository is exactly what the browser receives.

- **CSS** — one stylesheet; the palette and type scale live as custom properties in `:root`,
  so the whole page can be re-themed from a handful of lines
- **JS** — 53 lines: sticky-nav state, scroll reveal, active-section highlighting. Purely
  progressive enhancement; the page reads fine with JavaScript disabled
- **Icons** — an inline SVG `<symbol>` sprite referenced with `<use>`, so no icon font and
  no extra network requests
- **Images** — lazy-loaded, with intrinsic `width`/`height` set so nothing shifts as they load

## Structure

```
index.html            the whole page
css/style.css         all styling; palette and type scale in :root
js/main.js            sticky nav, scroll reveal, active nav link
assets/
  emma.jpg            portrait
  icon-32.png         favicon
  icon-180.png        apple-touch-icon
  og-image.jpg        social preview card (1200x630)
  logos/              institution logos
  projects/           project figures, reports and posters
.nojekyll             serve files verbatim, skip Jekyll processing
```

## Running it locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

Hard-reload with <kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>R</kbd> after editing CSS — browsers
cache stylesheets aggressively, and a normal reload will often serve the old one.

## Deployment

GitHub Pages serves `main` from the repository root. Every push redeploys automatically,
usually within a minute.

Two things worth remembering when editing:

- **Paths are case-sensitive on Pages** but not on macOS, so a mis-cased filename works
  locally and 404s once deployed.
- **The `og:` tags use absolute URLs.** If the domain ever changes, update them in
  `index.html` or social previews will break.
