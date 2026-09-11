# Dice Throne Draft Assistant

Mobile-first draft assistant for a friendly Dice Throne tournament. The app currently uses placeholder hero graphics and demo matchup data; the focus of the current versions is the draft workflow and recommendation logic.

## Version history

### v0.5
- Added linked official Dice Throne artwork for the heroes that have individual Digital Background downloads on the official Dice Throne site.
- Artwork is loaded remotely from the official Shopify CDN; no image files are bundled with the app.
- Hero cards use the linked artwork as a cropped background image.
- Heroes without a suitable official individual artwork URL still use placeholders for now.
- Player-complete state remains visually highlighted and can be toggled by tapping the player number again.

### v0.4
- Tapping the player number toggles whether all players are known.
- Open mode keeps `− / +`; `+` can add new players.
- Closed mode shows `← / →` and cycles through existing players only.
- Closed mode displays the current player as `Pcurrent/total` so the state is visible without another button.
- The player-complete state is included in Undo snapshots.

### v0.3
- Removed the picker/owner label from hero cards. Cards no longer show which player picked a hero.
- Heroes picked by `ME` are always pinned to the beginning of the grid, independent of score or alphabetical sorting.
- Added this README and version history.

### v0.2
- Removed the explanatory text describing tap and `×` behavior.
- `+` can create additional players dynamically, including after `ME` has been assigned.
- `ME` remains assigned while navigating to newly added players.

### v0.1
- Initial functional prototype.
- Four-column mobile hero grid with placeholder graphics.
- Player navigation with `−`, `+`, and `ME`.
- Tap a hero to record a pick for the current player.
- `×` removes a hero from the available pool.
- Undo support.
- Score and alphabetical sorting.
- Automatic score recalculation after picks.
- MAIN / FLEX / BAN role indicator.
- Known opponent picks influence the recommendation model.
- Roster overview for tracked players.

## Current limitations

- Some newer/licensed heroes still use placeholders until suitable official individual artwork URLs are identified.
- Hero strength and matchup values are demo data, not the final Dice Throne dataset.
- The recommendation model is functional but still needs the real matchup database and final calibration.

## Running locally

Open `index.html` in a modern browser. No server or build step is required.

## GitHub Pages

The app is fully static. `index.html` and this README can be placed in a GitHub repository and served directly with GitHub Pages.


## v0.6

- Originalgrafiken für die acht Marvel-Helden über offizielle Dice-Throne-Shop-CDN-Links ergänzt.
- X-Men-Portraits/Setups für Wolverine, Storm, Iceman, Psylocke, Cyclops, Gambit, Rogue und Jean Grey über The Op Games eingebunden.
- Outcasts-Grafiken für Pale Lady, Raveness, Necromancer und Headless Horseman über die offiziellen Dice-Throne-Hero-Pack-Bilder ergänzt.
- Alle Grafiken bleiben externe URLs; es werden keine Bilddateien lokal mitgeliefert.
- Platzhalter bleiben für Helden bestehen, für die noch keine passende offizielle Quelle eingetragen ist.

### Bildquellen v0.6

- Marvel: Dice Throne Store, Marvel Dice Throne Battle Chest.
- X-Men: The Op Games, Marvel X-Men Dice Throne Box 1 und Box 2.
- Outcasts: Dice Throne Store, jeweilige Hero Packs.


## v0.6.1

- Kritischen JavaScript-Syntaxfehler in der Bildquellen-Liste behoben, durch den das gesamte Heldenraster nicht gerendert wurde.
- Ursache war ein fehlendes Komma zwischen `Vampire Lord` und `Black Panther`.
- Keine Änderung an Draft- oder Score-Logik.
