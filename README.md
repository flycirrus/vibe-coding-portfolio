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
  link: { href: "https://…", label: "Live demo" }  // optional
}
```

- Add a project → add an object to the array.
- New `category` → a new filter chip appears on its own.
- No `link` → the card shows a "Private / client work" badge instead.

## Stack

Pure static site — HTML, CSS and vanilla JS, no build step. Deploys anywhere.

## Deploy

Static, zero-config on Vercel. Push to `main` and Vercel auto-builds, or run `npx vercel`.
