# 🎂 Happy Birthday, Thomas

An interactive 3D e-birthday card built with [three.js](https://threejs.org/) —
a ~30-second particle-morphing show with bloom glow, a synthwave grid, a
public-domain *Happy Birthday* chiptune, and full mobile + desktop support.

The particle cloud morphs through seven themed scenes:

1. **Happy Birthday** intro
2. **Thomas** title
3. **League of Legends** — a hextech crystal ("GG on Year ∞")
4. **The Wire** — a Baltimore skyline ("the game is the game")
5. **Beer** — a frosty mug ("Cheers!")
6. **McDonald's** — the golden arches ("i'm lovin' it")
7. **Fireworks finale**

## View it

Open `index.html` in any modern browser, or visit the GitHub Pages site once
Pages is enabled (Settings → Pages → Deploy from branch → `main` / root).

## How it works

Everything lives in a single `index.html`. three.js and its post-processing
addons load from a CDN via an import map, so there is no build step. Visuals are
generated procedurally: each scene is drawn to an offscreen 2D canvas, sampled
into points, and the ~4k–8k GPU particles ease between those point clouds.
Particle count, antialiasing, and pixel ratio scale down on mobile for smooth
performance.
