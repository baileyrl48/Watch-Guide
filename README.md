# Watch Guide

A phone-friendly guide to **where to stream** the next 7 days of NFL, college football, Gator basketball, Premier League and NBA games, with TV channels, live scores and a Steelers local-market check.

It's one static page. There's no server, API key or account to set up. Schedules come live from ESPN's public scoreboard data each time the page opens.

## Publish on GitHub Pages

1. Create a new **public** repository on GitHub (for example, `watch-guide`).
2. Upload everything in this folder: `index.html`, `manifest.webmanifest`, `icon.svg`, `icon-180.png`, `icon-192.png` and `icon-512.png`.
3. In the repo, go to **Settings → Pages**. Set Source to **Deploy from a branch**, Branch to **main** and the folder to **/ (root)**, then **Save**.
4. After a minute, the site is live at `https://YOUR-GITHUB-USERNAME.github.io/watch-guide/`.

## Share with the family

Send the link. Each person should:
- Tap **My services** and pick the streaming services they have. Their services are highlighted on every game. Choices are saved on that phone only.
- **Add it to the home screen** so it opens like an app. On iPhone (Safari), tap Share, then **Add to Home Screen**. On Android (Chrome), tap ⋮, then **Add to Home screen**.

## How the streaming info works

- ESPN lists each game's TV channel, plus any streaming-only service (Peacock exclusives, ESPN+, Prime Video, Netflix and so on).
- For TV channels, the page looks up which services carry that channel in the **`CARRIAGE` table** near the top of `index.html` (CBS → Paramount+, YouTube TV, …). Streaming deals change every season, so **check and edit that table** when a deal changes. It's plain text, one line per channel.
- NFL Sunday-afternoon CBS/FOX games also list **NFL Sunday Ticket** (out-of-market games). NBA games with no national broadcast list **NBA League Pass**.

## Steelers market badge

- **✓ In market:** the game is on a national broadcast (NBC, ESPN/ABC, Prime Video, NFL Network, Netflix) or a holiday CBS/FOX game.
- **? Check local map:** a regional Sunday-afternoon CBS/FOX game. The badge links to the 506 Sports coverage maps, because which regional game Knoxville gets isn't published as data.

## Changing things

- **Favorite teams:** `FAVS` in `index.html`.
- **Which college football games show:** `keepGame()` (currently ranked teams, big networks and all Gators games).
- **Streaming services list:** `SERVICES` and `CARRIAGE`.

ESPN's scoreboard feed is free but unofficial. If ESPN ever changes it, the page will show "Couldn't load" and the fetch code will need a small update.
