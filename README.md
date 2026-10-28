# India Oil Market Deep Dive

An interactive dashboard on how India kept importing crude through the 2026 Strait of Hormuz closure: the swing from Russian Urals to a Brent-priced crude basket, what it did to refinery output and product exports, and the price exposures that follow.

**Live site:** https://perion0x.github.io/india-oil-dashboard/

## What's inside

| Tab | Question it answers |
|---|---|
| Overview | How much crude did India import, and what changed in the slate? |
| 2026 vs 2021–25 range | Which series are outside their normal range, month by month? |
| Crude and the slate shift | Who supplied the barrels, and how did the basket move from Dubai to Brent? |
| Price and import bill | What happened to the basket price, refining margins and the import bill? |
| Refiners and yields | What do Indian refineries make from each crude grade? |
| Products: the proof | Do product exports confirm the crude slate really changed? |
| If Russia goes | What happens to output if Russian crude is replaced? |

Every chart reads from the files in `data/`, and each source is listed at the bottom of the page with a download link.

## Data

- **PPAC** (Petroleum Planning & Analysis Cell, Ministry of Petroleum and Natural Gas): monthly crude and product imports and exports, import values, Indian Crude Basket price and Brent/Dubai ratio, international product prices, refining capacity, demand and gas.
- **Mumbai Port Authority**: monthly rupee–dollar rate.
- **Kpler** ship-tracking estimates of crude suppliers, as reported by Business Standard and ThePrint (not official).
- **Refinery yield model**: indicative yields built from published crude assays. These are estimates, labelled as such on the page.

Trade data runs to September 2026 and prices to October 2026. FY2026-27 figures are provisional. Tonnes convert to barrels at 7.33 bbl/t.

## Update the data

1. Replace or edit the JSON in `data/`, keeping the same field names.
2. If you add a new source, add an entry for it in `data/datasets.json`.
3. Run `python tools/build_data.py` to regenerate `data.js`.
4. Commit and push. GitHub Pages republishes automatically.

To preview locally, open `index.html` in a browser. No server or build step is needed.

## Built with

Plain HTML and JavaScript with [d3 v7](https://d3js.org) (bundled in `vendor/`). No frameworks, no tracking, works offline.
