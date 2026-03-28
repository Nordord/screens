# screens.nordord.fi

Full-screen HTML display pages for wall screens, TV browsers, and digital signage.

Hosted via GitHub Pages at [screens.nordord.fi](https://screens.nordord.fi).

## Screens

| File | Style | Description |
|------|-------|-------------|
| `teksti-tv.html` | YLE Teksti-TV / P100 | Black background, phosphor palette, authentic 80s Finnish teletext aesthetic inside a CRT TV frame |
| `tvshop.html` | 90s Finnish TV Shop | Chroma-key teal, starburst price tags, flashing banners — peak bad taste, executed with precision |
| `solari-board.html` | Helsinki Rautatieasema | Split-flap Solari departure board with per-character flip animation |

## Data source

All screens pull live news from the [YLE RSS feed](https://feeds.yle.fi/uutiset/v1/majorHeadlines/YLE_UUTISET.rss) via [rss2json.com](https://rss2json.com) as a CORS proxy. Requests are made directly from the viewer's browser. No backend, no build step.

Feed: `https://feeds.yle.fi/uutiset/v1/majorHeadlines/YLE_UUTISET.rss`  
Proxy: `https://api.rss2json.com/v1/api.json?rss_url=<feed>`

News headlines link directly to the original YLE articles.

Auto-refreshes every 10 minutes.

## Usage

Open any HTML file directly in a browser. Works fullscreen on any display or TV browser. No dependencies, no build tools, no frameworks — plain HTML, CSS, and vanilla JS.

## Tech

- Zero dependencies
- No build step
- Self-contained single-file pages
- Designed for 16:9 and 4:3 displays
- CRT TV shell frame shared across screens (NORDOVISION NV-100)

## Adding screens

Each screen is a standalone HTML file. Drop a new file in the repo root and it's live.

Planned: shared live data structure `{hl, body, cat, time}` to decouple fetch logic from presentation.

---

*Nordord Oy — [www.nordord.fi](https://www.nordord.fi)*
