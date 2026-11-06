# Photographs Taken per 5 Years

A bar chart of the estimated number of photographs taken worldwide per year, sampled every five years from 1975 to 2025.

## Prompt

> Please generate a bar chart Visualizer of the number of photographs taken estimated in 5-year intervals for the last 50 years

## What it shows

- **11 bars** (1975, 1980 … 2025), rising from about 15 billion to about 2.1 trillion photos a year, roughly a 140-fold increase.
- **Two colors:** grey for the mostly-film years (1975–2000) and blue for the mostly-digital/smartphone years (2005–2025).
- **Log-scale toggle:** on a linear scale the film years look almost flat; the button switches the y-axis to logarithmic so the early growth is visible.
- **Tooltips** show each value (e.g. "~2.1T photos").
- Follows the system light/dark mode.

## Data and caveats

| Year | Photos/year | Basis |
|---|---|---|
| 1975 | ~15B | rough reconstruction |
| 1980 | ~25B | rough reconstruction |
| 1985 | ~40B | rough reconstruction |
| 1990 | ~57B | rough reconstruction |
| 1995 | ~70B | rough reconstruction |
| 2000 | ~86B | rough reconstruction (film peak) |
| 2005 | ~150B | rough reconstruction |
| 2010 | ~350B | rough reconstruction |
| 2015 | ~1T | estimate between 2010 figures and InfoTrends' ~1.2T for 2017 |
| 2020 | ~1.15T | published estimate (pandemic dip) |
| 2025 | ~2.1T | published estimate |

The 1975–2010 figures came from the model's general knowledge (mostly old film-sales estimates) and were not checked against a source, so treat them as approximate.

Sources for the recent figures:
- [Photutorial – Photo statistics](https://photutorial.com/photos-statistics)
- [16best – How many photos are there](https://16best.net/how-many-images-are-on-the-internet/)
- [Statista – Number of photos taken worldwide](https://statista.com/chart/amp/10913/number-of-photos-taken-worldwide)

## How it was made

Claude ran a web search for current photo-count estimates, then generated the chart as an inline chat widget using [Chart.js 4.4.1](https://www.chartjs.org/). For this repo the widget code was wrapped in a standalone HTML page, with small CSS stand-ins for the theme variables the chat interface normally supplies. The chart code itself is unchanged.

## Run it

Open `index.html` in a browser (an internet connection is needed to load Chart.js from the CDN).
