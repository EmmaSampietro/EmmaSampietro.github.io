# emmasampietro.github.io

Personal website. Plain static HTML/CSS/JS — no build step, no dependencies.

## Structure

```
index.html                     single page: hero, about, experience, projects, education
css/style.css                  all styling; palette lives in the :root custom properties
js/main.js                     sticky-nav state, scroll reveal, active nav link
assets/emma.jpg                hero portrait
.nojekyll                      serve files verbatim, skip Jekyll
```

## Preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. Hard-reload (Cmd+Shift+R) after editing CSS.

## Publishing to GitHub Pages

The repo is **private** while the design is being worked on. GitHub Pages does not serve
private repos on the free plan, so there is no live URL yet.

To go live:

1. **Settings → General → Change visibility → Public**
2. **Settings → Pages → Source: _Deploy from a branch_ → Branch `main` / `/ (root)` → Save**

The site appears at <https://emmasampietro.github.io> within a minute or two. After that,
every push to `main` redeploys automatically.

