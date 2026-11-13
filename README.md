# Catchr — GitHub Pages static site

A zero-backend, zero-login vintage Pokémon promo archive. Fully static HTML, CSS, and JavaScript. All 88 starting card records are **bundled** in `cards.js`, so there are no network calls to fetch card data.

## Publish on free GitHub Pages

1. Create a public repository on GitHub, e.g. `catchr`.
2. **Upload the *contents* of this folder** (`index.html`, `styles.css`, `app.js`, `cards.js`, `cards.json`, `assets/`, etc.) to the **root** of the repository. Do not upload the ZIP itself.
3. In your repository go to **Settings → Pages → Build and deployment → Deploy from a branch**, choose `main` and `/ (root)`, then **Save**.
4. Open the Pages address shown in GitHub Pages settings (typically `https://YOUR-USERNAME.github.io/catchr/`).

You can also open `index.html` on your computer without a server. The card records load even using `file://`.

## What works

- Mobile-friendly layout and expandable sidebar
- Instant local search across card name, number, year and campaign
- Year, language, finish, and sorting filters
- Collection navigation, quick-year buttons, grid/list toggle, and card detail panels
- Starred watchlist (saved in **this browser's** local storage; no syncing)
- 88 distinct printings from McDonald's Japanese 2002–2007 campaigns
- GBP raw/PSA 10 *indicative* historical guide fields and PSA 10 population where present in the supplied source spreadsheet
- All card data editable in one local `cards.js` file; machine-readable copy in `cards.json`

## Important: images and research status

**Actual card photographs have NOT been embedded**. Every card has a carefully designed generic local placeholder and a link to a Google Image search for the specific printing. This is deliberate: we did not have verified, reusable artwork for all 88 cards and did not want to display mismatched cards. Card data is entirely local; card photo searches are optional external links. The decorative heading font is optionally loaded from Google Fonts; local fonts take over offline.

For actual local images, save authorized, verified card photos under `assets/cards/`, with filenames matching each card's `id` in `cards.js` (such as `2002-squirtle-007-018-holo.webp`) and change that card's `image` field from `null` to `assets/cards/FILENAME.webp`. No backend changes are required. Before publishing card photos, verify licensing/permission and the exact card printing.

**2000–2010 is the intended scope, NOT the completed content scope.** The starter dataset contains **88 Japanese McDonald's printings from 2002–2007 only**. Movie, retail, tournament and other campaigns appear as empty/planned navigation. English, Indonesian and other languages remain data-model ready but have not been researched/added yet. Indonesian-language Pokémon TCG releases only began after this archive period.

The raw/graded values imported from the earlier spreadsheet are **unverified estimates**, not recent sold listings or investment-grade prices. Never treat unknown glossary/foil/exclusivity fields as confirmed. `Japanese campaign only` indicates Japanese distribution for this campaign, not that no card with similar artwork has appeared elsewhere.

## Extend the dataset

Each object in `cards.js` contains: `id`, `name`, `number`, `year`, `language`, `region`, `category`, `campaign`, `series`, `finish`, `glossy`, `exclusivity`, `exclusivityNotes`, `raw`, `rawStatus`, `psa10`, `pop10`, `psaStatus`, `photoSearch`, `image`.

- `id` must be unique per printing.
- Monetary fields are GBP numbers (e.g. `95`) or `null` if not verified.
- `finish` is plain text; keep each distinct holo/non-holo/glossy printing as a separate row.
- Update both `cards.js` and `cards.json` when changing the archive.
- To add a category with results, give new records a matching `category` and add the category button to the page (some placeholder categories exist already).

## Source

Starter data: provided `pokemon_promo_archive_2000_2010_v1.xlsx`. Images and current market prices require future independent verification.

Independent fan project, not endorsed by Pokémon, Nintendo, Creatures, Game Freak or McDonald's.
