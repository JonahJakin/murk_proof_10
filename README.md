# MURK

A first-person underwater survival horror game built with Three.js. One diver enters a drowned freshwater landscape to recover evidence of something far too large for the lake. Demo V10 adds a waterline view of the workboat to the title tableau, a properly rim-mounted helmet lamp, a subtly clearer mountain silhouette through the depth-aware fog, denser cliff-safe weed colonies, more readily heard passive creature calls, consolidated found-footage readouts, and a pause menu that only lists controls not already shown on the HUD.

The world, creature, effects, map illustrations, and true-grid pixel icon are generated in code. Creature calls use the supplied, conservatively cleaned WAV recordings; suit, water, breath, and interaction sounds remain procedural.

## Controls

- `WASD` swim; mouse or arrow keys look
- `Space` dive while standing at an edge of the boat and looking out, then rise underwater
- `Shift` descend
- `F` raise or stow the carried floodlight
- `L` main lamp
- `Q` raise or stow the camera
- `E` camera shutter (while the camera is raised)
- `M` raise or fold the map
- `C` hold breath
- `G` raise and ping the directional sonar; its latest contact remains on the map
- `X` take evidence
- `R` deploy a sinking decoy light
- `B` emergency air boost
- `Esc` pause the game and all audio; use Continue to resume

The pause menu also toggles the optional **Found Footage** visual mode.

Breaking the surface gradually refills the tank. Dense Curtain weed can conceal the diver even with the helmet lamp lit; the similar-looking Sparse weed cannot.

Restart resets the dive in place and returns the player to the boat without leaving the pause menu active.

## Run locally

```bash
pnpm install
pnpm dev
```

Build the hosted version with `pnpm build`.

## Installable PWA

MURK includes a web app manifest, maskable and Apple app icons, and an offline service worker. Build the standalone static PWA with:

```bash
pnpm build:pwa
```

The deployable static files are written to `pwa-dist/`.

## Publish with GitHub Pages

The repository includes `.github/workflows/deploy-pwa.yml`. Push the project to a GitHub repository, then choose **GitHub Actions** as the Pages source in the repository settings. Pushes to `main` build and publish the standalone PWA automatically.

The Sites build and GitHub Pages PWA share the same game source, controls, procedural visuals, and spatialized audio library.
