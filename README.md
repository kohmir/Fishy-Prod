# Abyssal Cast

A retro pixel fishing game. This repository contains the compiled static build.

The Schoolkeeper Rig adds capacity for two, three, and four fish. The first bite
starts reeling; fill the spare hooks with more catches on the way up. Astral
Harpoon Alloy adds one bonus slot, for a maximum of five fish per cast.

The expansion brings the collection to 35 animated species, with biome-exclusive
catches, three specialist hook fittings (one equipped at a time), and a Turbo
downward burst. Waters end at 300m, 650m, 1,000m, and 1,500m; Turbo upgrades from 2 to
8 seconds and from one to three uses per cast.

The fourth biome, Sunken Glacial Fjord, adds icy continuous parallax scenery,
Frostglass Char, Tusked Icewolf, and the Level 6 Rimejaw Megalodon. Tier 4 tackle
adds 1,500m line reach, two faster sinker levels, and Level 6 hook strength.

The abyssal balance update adds five animated Common/Uncommon obstacles and
independent rarity rolls. Mythics have a 5.88–10% deep-water roll with at least
100m between Mythic spawns. Encounter spacing widens with depth to 16–18m.

## GitHub Pages

In Settings → Pages → Build and deployment, select **Deploy from a branch**,
**main**, and **/(root)**. All game files are already at the repository root.

The game works under this repository's `/Fishy-Prod/` subfolder. No server
or API keys are needed. Player progress is stored locally in each browser.

## Updating

Build the source with `npm run build:pages`. Replace the generated `index.html`,
`assets/`, `art/`, and `fonts/` with the contents of the new `dist/`, removing
obsolete hashed assets. Preserve this README and `.nojekyll`, then commit and
push to `main`. GitHub Pages deploys the updated files.
