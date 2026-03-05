# fractal-art

A realtime fractal art playground built with Astro and Three.js.

## Highlights

- 11 signed-distance fractal modes (Mandelbulb, Mandelbox, Julia 3D, and more)
- Ray-marched shader with improved lighting, ambient occlusion, soft shadows, and fog
- Post-processing pipeline (ACES tone mapping, bloom, chromatic aberration, vignette)
- Live controls for scale, iterations, morphing, bloom, glow, and render quality
- Adaptive quality mode that tunes trace budget/pixel density for smoother frame times
- Responsive UI that works on desktop and mobile

## Tech Stack

- Astro 5
- Three.js
- GLSL fragment shader raymarching

## Quick Start

```bash
npm install
npm run dev
```

Open `http://localhost:4321`.

## Available Scripts

- `npm run dev`: Start local development server
- `npm run build`: Build for production
- `npm run preview`: Preview production build
- `npm run check`: Run Astro project checks

## Controls

- Left panel: choose fractal type
- Right panel: tune fractal and render parameters
- Mouse/touch drag: orbit camera
- Scroll/pinch: zoom

## Optimization Notes

- Rendering uses adaptive trace budget and capped pixel ratio scaling
- Auto-quality watches recent frame times and adjusts quality dynamically
- Camera distance per fractal is preset to reduce clipping and improve framing

## Project Structure

```text
.
├── public/
├── src/
│   ├── components/
│   │   └── Mandelbulb.astro
│   └── pages/
│       └── index.astro
├── astro.config.mjs
└── package.json
```

## License

MIT
