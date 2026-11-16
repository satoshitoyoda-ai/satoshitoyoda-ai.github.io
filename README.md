# Pikomori ピコモリ

A little forest of homemade games and learning apps for kids. The site is static (plain HTML, no build step) and is served by GitHub Pages.

- **No ads, no accounts, no analytics.** Nothing is sent anywhere. Names and progress stay in the browser's local storage on the device that plays.
- **No third-party requests.** No web fonts, CDNs or trackers. Games use the device's own fonts and voices.
- **No speech recognition.** It is switched off in the public copies, because some browsers send that audio to a server.
- **Not indexed.** Every page carries `robots: noindex`, so the site is shared by link.
- **Original characters only.**

## What is where

| Path | What |
|---|---|
| `index.html` | Home page: all games with age groups, Japanese / English switch (follows the device language and remembers the choice) |
| `manifest.json`, `icon-*.png`, `favicon.svg` | Add to Home Screen |
| `draw-with-me/`, `dino-blaster/`, `sky-patrol/`, `pop-it/`, `bubble-sniper/`, `color-blocks/`, `nihongo-picnic/`, `math-walk/`, `cupcake/` | One game per folder (`index.html`, plus icons and a manifest for some) |
| `/abc123/`, `/dino-ranger/`, `/reef-ranger/` | Separate repositories (their own GitHub Pages project sites), linked from the home page |

## Adding or updating a game

The game folders are generated from the working copies by a private build step that also removes personal details and runs a safety check. Do not edit the game folders by hand. Re-run the build, then the check, then commit.

To add a game: add its card to `index.html`, with `data-groups="little"` (ages 3–5), `"big"` (ages 6+) or both.
