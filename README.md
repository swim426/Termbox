# Termbox — GitHub Pages setup

This folder is a starter website for Termbox, including a shared deck library and the Human Skeleton deck.

## Publish it for free

1. Sign in to GitHub (create a free account if needed).
2. Create a **public** repository named `termbox`.
3. Upload **the contents of this folder** to the repository root. Make sure `index.html` is at the top level, with `decks.json` and the `decks/` folder beside it.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**, choose the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish. The site address will look like `https://YOUR-USERNAME.github.io/termbox/`.

Your friends do not need GitHub accounts. Share the website address.

## Add another shared deck

1. Export a deck from Termbox using **Export deck** (not Export backup).
2. Upload that JSON file into the repository's `decks/` folder.
3. Edit `decks.json` and add another object to the `decks` array, using the deck's exact `id` from its JSON file. Example:

```json
{
  "id": "biology-basics",
  "name": "Biology Basics",
  "description": "Introductory biology terms.",
  "file": "decks/biology-basics.json"
}
```

4. Commit the changes. After GitHub Pages updates, users can open Termbox and tap **Refresh** in Shared deck library.

Deck files must be Termbox **deck exports** (`format: "termbox-deck"`, version 1), not full backups. The shared catalog is `decks.json` (`format: "termbox-deck-catalog"`, version 1).

## Important notes

- Keep the repository public for the free, no-login sharing workflow. Anyone can view and download its contents.
- Study progress is stored separately in each user's browser. Adding/updating a shared deck preserves progress for matching card IDs; newly added cards start fresh.
- This version does not synchronize progress between devices.
- The website needs to be hosted online for the shared catalog to load. Opening `index.html` directly from a local file will not load the shared catalog.
- Keep `index.html`, `decks.json`, and the `decks/` folder at the repository root as shown.
