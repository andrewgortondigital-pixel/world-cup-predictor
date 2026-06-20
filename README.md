# World Cup 2026 Predictor

A self-contained web app showing the FIFA World Cup 2026 group standings, the full
knockout bracket, live results, and odds-led predictions all the way to a projected champion.

- **`index.html`** — the entire app (HTML + CSS + JS, no dependencies, no build step).
- Predictions run client-side: team strengths anchored to betting odds, a Poisson match
  model, and a Monte-Carlo simulation of every remaining match.

## Updating

The data lives in the `DATA` block in `index.html`, between the markers
`<<<WC_DATA_START>>>` and `<<<WC_DATA_END>>>`. A scheduled task refreshes it each morning
with the previous day's results and the latest odds, then commits and pushes — Netlify
redeploys automatically.

## Hosting

Static site on Netlify. Publish directory is the repo root (see `netlify.toml`).
