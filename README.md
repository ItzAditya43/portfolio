# Aditya's Village — 3D Portfolio

A single-file, fully 3D portfolio built with [Three.js](https://threejs.org/) — an animated floating Japanese village you fly around instead of scrolling through a page. Visit shrines to read About / Projects / Stack / Contact, walk past NPC villagers who have their own lines, and watch it shift through a real-time day/night cycle and four seasons.

**Live:** [itzaditya43.github.io/portfolio](https://itzaditya43.github.io/portfolio/)

## Features

- **Procedural island** — terrain, paths, trees, grass, and boulders generated at load time from value noise, no external assets
- **4 interactive shrines** — About, Projects, Stack & Currently, Contact — reached by torii gates and a generated village road network
- **Living villagers** — wander the island on waypoints, speak occasional lines, clickable for a short bio
- **Real-time day/night cycle** — sun/moon position, sky color, and lantern glow all track the actual system clock
- **Seasons** — spring/summer/autumn/winter each with their own palette, sky, and falling particles (blossoms, leaves, snow)
- **Realistic rendering** — procedurally textured materials (grass, wood grain, shingles, stone), image-based sky lighting, soft shadows, and a post-processing pipeline (bloom, gamma correction, vignette)
- **Adaptive performance** — auto-detects mobile and scales down shadow/texture/particle quality, drops the costliest lights, and dynamically adjusts render resolution to hold frame rate on any device
- **Touch & mouse controls** — drag/one-finger to orbit, scroll/pinch to zoom, tap/click to interact

## Tech

Vanilla JS + [Three.js r128](https://github.com/mrdoob/three.js/) (CDN), no build step, no dependencies to install. Everything — geometry, textures, shaders, UI — lives in `index.html`.

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
| Scroll / pinch | Zoom |
| Click / tap a shrine or villager | Open its card |
| Return to overview | Exit the current shrine/villager view |

## About

Built by [Aditya Pandey](https://github.com/ItzAditya43) — AI/ML and full-stack developer. See the Shrine of Beginnings and Shrine of the Old Pine in the village itself for more.
