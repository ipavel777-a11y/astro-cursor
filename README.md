# astro-cursor

A minimal [Astro](https://astro.build) site, configured to run out-of-the-box in
Cursor Cloud Agents.

## Prerequisites

- Node.js `>=22.12.0` (the repo is tested with Node 22)
- npm (ships with Node)

## Getting started

```sh
npm install
npm run dev
```

The dev server starts on [http://localhost:4321](http://localhost:4321).

## Scripts

| Command           | Action                                             |
| ----------------- | -------------------------------------------------- |
| `npm install`     | Install dependencies                               |
| `npm run dev`     | Start the local dev server at `localhost:4321`     |
| `npm run build`   | Build the production site to `./dist/`             |
| `npm run preview` | Preview the production build locally               |
| `npm run astro`   | Run Astro CLI commands (e.g. `astro check`)        |

## Project structure

```text
/
├── public/              # Static assets served as-is
├── src/
│   ├── components/      # Reusable Astro components (e.g. Counter island)
│   ├── layouts/         # Shared page layout + global styles
│   └── pages/           # File-based routes (index.astro)
├── astro.config.mjs
└── package.json
```

## Cloud Agent environment

The `.cursor/environment.json` file defines how this project boots in Cursor
Cloud Agents:

- `install` runs `npm install` after checkout.
- The `astro-dev` terminal runs `npm run dev` bound to `0.0.0.0:4321` so the
  running dev server is visible and reachable during agent sessions.
