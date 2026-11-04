# CENTCOM NC

Combined local intel for St. Lawrence County: scanner, events, campus, business, and news in one stream.

## How it works

- `index.html` — the whole page. One file, no build step. It loads `data/items.json` at runtime; feeds update the data without ever touching the page.
- `data/items.json` — the stream. Every item is one normalized record answering what / where / when / who / why, with a category (`scanner`, `event`, `campus`, `business`, `news`), a source name + link, first-seen and updated stamps, and a confidence value.
- One story = one item, forever. Developing stories update in place; they never spawn duplicate cards.
- Items expire: scanner after 48 h, news after 7 days, events at start + 3 h. The file is a rolling window, not an archive.

Design law, in one line: if an element doesn't help answer what is going on, where, when, why, and who — it doesn't ship.

Status: draft preview with sample items, ahead of the live feed wiring.
