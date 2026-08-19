# Tejero's Take Texas

A single-page, mobile-friendly itinerary site for the cousins' Houston trip
(Sept 4–7). Neon Texas theme, scroll-driven sunset background, sticky-card
layout.

## Structure

Everything lives in one self-contained `index.html` — no build step, no
dependencies, no backend. The neon sign artwork is embedded directly as a
base64 image, so there's nothing else to host.

## Local preview

Just open `index.html` directly in a browser, or serve it locally:

```bash
npx serve .
```

## Deploying

This repo is set up to deploy on [Vercel](https://vercel.com) with zero
configuration — it's a static `index.html` at the project root, so Vercel
will serve it as-is. Connect this repo in the Vercel dashboard and it'll
auto-deploy on every push to `main`.

## Updating the itinerary

Times, activities, links, and images are all plain HTML inside `index.html`
under the `<!-- DAY 1 -->` through `<!-- DAY 4 -->` comments. The sunset
color logic and scroll effects live in the `<script>` block near the bottom
of the file.
