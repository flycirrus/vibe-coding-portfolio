# Vibe Coding Portfolio — Renaldo Recchiuti

A single-page catalog of the web apps I've built with AI-assisted "vibe coding",
across aviation, pilot training, operations and business.

**Live:** _(Vercel URL after deploy)_

## Edit the catalog

All projects live in the `PROJECTS` array inside `index.html`.
Each entry:

```js
{
  title: "App name",
  category: "Aviation & Ops",   // drives the filter chips automatically
  desc: "One or two sentences.",
  tech: ["Next.js", "Prisma"],
  status: "live",               // live | public | private | dev
  img: "assets/app.png",        // screenshot thumbnail (optional)
  icon: "🛫",                   // fallback emoji icon if no screenshot
  link: { href: "https://…", label: "Open app" }  // optional
}
```

- Add a project → add an object to the array.
- New `category` → a new filter chip appears on its own.
- `img` → card shows that screenshot (put the file in `assets/`); else `icon` emoji on a gradient.
- No `link` → the card shows a "Private / client work" badge instead.

### Refreshing screenshots

Thumbnails in `assets/` are headless-Chrome captures of the live apps
(1280×800, resized to 760px wide). Re-capture any app with:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless=new --window-size=1280,800 --virtual-time-budget=9000 \
  --screenshot=assets/NAME.png "https://NAME.vercel.app"
sips --resampleWidth 760 assets/NAME.png
```

## Stack

Pure static site — HTML, CSS and vanilla JS, no build step. Deploys anywhere.

## Deploy

Static, zero-config on Vercel. Push to `main` and Vercel auto-builds, or run `npx vercel`.
