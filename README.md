# Catchr V4 — static GitHub Pages release

## Install
Upload the contents of this folder, keeping `index.html` in the repository root and the `assets/` directory intact. No backend or authentication needed. For iPhone single-file installation, use the accompanying `Catchr_V4_iPhone_index.html`, rename to `index.html`, and upload as one file instead.

## What is included
- 326 card records, 82 distinct McDonald’s catalogue entries and 52 movie/cinema entries.
- 82 **locally stored placeholder SVGs** for McDonald’s, each with a clean X and the card number.
- **0 genuine McDonald’s scans in this release.** The remote scan hosts could not be downloaded here. The website does not fetch remote McDonald’s images at runtime.
- Card-to-file mapping in `assets/cards/mcdonalds/image-manifest.csv`, including research URLs where previously identified.
- Search, filters, card details, categories, no favourites/watchlist, no backend.
- Other categories may still have remotely hosted image references.

## Replace missing art
For a card, save your licensed/exact card scan in `assets/cards/mcdonalds/` under a stable filename and change its `image` path and `imageIsPlaceholder:false` in `cards.json` and `cards.js`. The IDs uniquely identify cards for safe future expansion.

If the requirement is actual scans rather than X placeholders, do not mistake this for a finished image collection.
