# Aditya's Village — 3D Portfolio

A single-file, fully 3D portfolio built with [Three.js](https://threejs.org/) — an animated archipelago of floating Japanese villages you fly around instead of scrolling through a page. Visit shrines to read About / Projects / Stack / Contact, walk past NPC villagers who have their own lines, and watch it shift through a real-time day/night cycle and four seasons.

**Live:** [itzaditya43.github.io/portfolio](https://itzaditya43.github.io/portfolio/)

## Features

- **Procedural archipelago** — a hub plaza ringed by four floating islands at different heights, joined by arched bridges; terrain, paths, trees, grass and boulders are generated at load time from value noise, no external assets
- **4 shrine islands, each with its own character** — About has a koi lake ringed with stones, Projects a ridged rock massif where a stream drops over a horseshoe cliff into a plunge pool, Stack fenced farm fields (wheat, rice paddy, cabbages, pumpkins, a scarecrow), and Contact a bamboo grove where a sage keeps watch by the shrine. Each also has its own houses, square and residents
- **Living villagers with jobs** — 26 residents, each a named character whose role explains part of the portfolio (the Blacksmith talks Zenith, the Observatory Keeper Trace, the farmers the tech stack, the Letter Writer how to get in touch). They live on a home island, cross bridges to visit, stop to chat, and their cards link to the project they speak for
- **Real-time day/night cycle** — sun/moon position, sky color, and lantern glow all track the actual system clock
- **Seasons** — spring/summer/autumn/winter rotate on a 90-second timer, each with its own palette, sky, and falling particles (blossoms, leaves, snow)
- **Realistic rendering** — procedurally textured materials (grass, wood grain, shingles, stone), image-based sky lighting, soft shadows, and a post-processing pipeline (bloom, gamma correction, vignette)
- **Adaptive performance** — auto-detects mobile and scales down shadow/texture/particle quality, drops the costliest lights, and dynamically adjusts render resolution to hold frame rate on any device
- **Atmosphere** — fields of red spider lilies (higanbana), a sacred tree on the plaza whose canopy follows the season, sky lanterns and fireflies after dusk, drifting islets, a denser starfield and an opening camera sweep
- **Vegetation and sky** — 30,000 instanced grass tufts that sway in a vertex-shader wind, multi-lobed tree crowns with alpha-tested leaf cards, a sky shader with horizon haze and sun/moon glow, and a cratered moon disc
- **Theme** — colours from my Higanbana project (true black, neutral greys, spider-lily red, gold); shapes and type from Higanbana and Sourcemark (elevated cards, serif display headings, Inter/Sora UI text, mono tags)
- **Portfolio layer** — intro with name and role, a section nav bar (About / Projects / Stack / Contact), and an "All work" list view with every project, stack, background and contact links for visitors who would rather read than fly
- **Deep links** — `#about`, `#projects`, `#stack`, `#contact` and `#work` open that section directly; `Esc` closes it
- **Fallback** — if WebGL or the Three.js CDN is unavailable, the list view is shown instead of a blank page
- **Touch & mouse controls** — drag/one-finger to orbit, scroll/pinch to zoom, tap/click to interact

## Tech

Vanilla JS + [Three.js r128](https://github.com/mrdoob/three.js/) (CDN), no build step, no dependencies to install. Everything — geometry, textures, shaders, UI — lives in `index.html`.

## Editing the content

All text (bio, projects, stack, links) lives in one data block near the top of the `<script>` in `index.html` (`PROFILE`, `FEATURED`, `MORE`, `STACK`, `NOW`, `BACKGROUND`). The shrine cards and the list view are both generated from it. To show a Résumé link, put the PDF in this folder and set `PROFILE.resume`.

## Running locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Controls

| Input | Action |
|---|---|
| Drag / one-finger swipe | Orbit camera |
| Right-drag / Shift-drag / two-finger drag | Move the view across the islands |
| W A S D / arrow keys | Move the view; Q and E turn |
| Scroll | Zoom toward the cursor, so you travel to where you point |
| Double-click ground | Fly there |
| Scroll / pinch | Zoom |
| Click / tap a shrine or villager | Open its card |
| Return to overview | Exit the current shrine/villager view |

## About

Built by [Aditya Pandey](https://github.com/ItzAditya43) — AI/ML and full-stack developer. See the Shrine of Beginnings and Shrine of the Old Pine in the village itself for more.
