# Through Smoke and Code

Browser-based first-person 3D game prototype using Three.js, Rapier physics, TypeScript, and Vite.

## Features in the source

- A WebGL scene and first-person camera.
- Rapier physics world and player movement.
- Pointer-lock mouse look, WASD movement, and jumping.
- GLB assets under `public/`.

## Run locally

The repository includes a Bun lockfile and package scripts:

```bash
bun install
bun run dev
```

Click the scene to capture the mouse. Use WASD to move, Space to jump, and Escape to release the mouse.

## Build and deployment

`bun run build` runs TypeScript checking followed by a Vite build; `bun run preview` previews the result. Once the build and asset loading are verified, `dist/` is the static-hosting output. Live demo: https://adityakumar027.github.io/through-smoke-and-code-main/

Hosted on GitHub Pages from `main/docs`, using locally built static files. The deployed bundle is `docs/4-app.js`, with its map asset alongside it. Source edits do not automatically rebuild that bundle: run the checked build, regenerate the Pages-base output, and replace the published files together.

This is a movement/scene prototype, not a complete multiplayer shooter. The imported map currently uses a simple ground collider, not detailed building collisions.
