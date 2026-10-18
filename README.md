# Abyssal Cast

A retro pixel fishing game. This repository contains the compiled static build.

## GitHub Pages

In Settings → Pages → Build and deployment, select **Deploy from a branch**,
**main**, and **/(root)**. All game files are already at the repository root.

The game works under a repository subfolder, such as `/Fishy-pages/`. No server
or API keys are needed. Player progress is stored locally in each browser.

## Updating

Build the source with `npm run build:pages`. Replace the generated `index.html`,
`assets/`, `art/`, and `fonts/` with the contents of the new `dist/`, removing
obsolete hashed assets. Preserve this README and `.nojekyll`, then commit and
push to `main`. GitHub Pages deploys the updated files.
