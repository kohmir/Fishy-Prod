# Deepcast

A retro pixel fishing game. This repository contains the compiled static build.

The Schoolkeeper Rig adds capacity for two, three, and four fish. The first bite
starts reeling; fill the spare hooks with more catches on the way up. Astral
Harpoon Alloy adds one bonus slot, for a maximum of five fish per cast.

The expansion brings the collection to 36 animated species, with biome-exclusive
catches, three specialist hook fittings (one equipped at a time), and a Turbo
downward burst. Waters end at 300m, 650m, 1,000m, and 1,500m; Turbo upgrades from 2 to
8 seconds and from one to three uses per cast.

The fourth biome, Sunken Glacial Fjord, adds icy continuous parallax scenery,
Frostglass Char, Tusked Icewolf, and the Level 6 Rimejaw Megalodon. Tier 4 tackle
adds 1,500m line reach, two faster sinker levels, and Level 6 hook strength.

The abyssal balance update adds five animated Common/Uncommon obstacles and
independent rarity rolls. Mythics have a 5.88–10% deep-water roll with at least
100m between Mythic spawns. Encounter spacing widens with depth to 16–18m.

Species mastery awards stars at 1, 10, and 30 lifetime catches. Two stars grant
a permanent +10% value bonus for that species; three stars replace it with +20%.
Existing catch records count automatically, with progress shown in the journal.

Aurora Crown Dory is a Level 5 rare exclusive to the Glacial Fjord at
1,000–1,500m, with original pixel art and animated crown, fins, and tail.

The field journal uses compact cards; tap one for full lore, catch requirements,
mastery, and records. Keyboard navigation and short-screen detail dialogs are supported.

On touchscreens, touch the scene and drag left/right from your starting point
to steer. Each gesture has a small neutral zone and a floating pixel joystick.
Desktop mouse and keyboard controls retain their original behavior.

Fish animations are prepared ahead of time and preloaded behind the loading
screen. Journal previews draw only when visible. Joystick painting and HUD
updates avoid redundant rendering; hidden or paused lakes skip repainting.

The Lake Drifter boat icon uses Whispering Pine Lake's colors and appears in browser tabs, the game header, and the
loading screen. Apple Touch Icons include 180px iPhone and 167/152px iPad variants;
home-screen labels use Deepcast. Existing player saves remain compatible.

## Current build

Includes the animated surface cast, articulated fisherman arms, splash and smooth
underwater camera follow across all four biomes. The boat sits to the left with
its stern slightly outside the frame. Casting respects pause; catches and Turbo
begin after water entry. New species catches display a readable New badge.
Landed fish leave the live hook immediately; closing the catch summary reveals
the empty hook and bait reset to the ready position for another cast.

New biome unlocks require 12 discovered species for the Cenote, 20 for the
Caldera, and 28 for the Fjord. Unlock costs remain 650 / 1,800 / 4,200 coins,
and already-unlocked waters remain available.

All four biomes now use complete pixel panoramas, with Pine Lake’s expanded
rose-and-gold sunset, the Cenote canopy, Caldera stars and Fjord aurora reaching
from the top of the view to the water. The scenery stays anchored during casting;
underwater parallax remains intact.

Full hooks ease from normal speed to 4× over 1.5 seconds, then ease back to
normal over the final 20 metres. Shallow catches smoothly blend both phases;
spare slots and empty hooks retain their existing ascent speeds.

Source commit: `c4ded75dab8567e64394a56ceb40940459012f5a` (PR #13). See `build-info.json`
for build metadata. The source PR remains open; this repository hosts its tested
compiled production build.

## GitHub Pages

In Settings → Pages → Build and deployment, select **Deploy from a branch**,
**main**, and **/(root)**. All game files are already at the repository root.

The game works under this repository's `/Fishy-Prod/` subfolder. No server
or API keys are needed. Player progress is stored locally in each browser.

## Updating

Build the source with `npm run build:pages`. Replace the generated `index.html`,
`assets/`, `art/`, `fonts/`, and `icons/` with the contents of the new `dist/`, removing
obsolete hashed assets. Preserve this README and `.nojekyll`, then commit and
push to `main`. GitHub Pages deploys the updated files.
