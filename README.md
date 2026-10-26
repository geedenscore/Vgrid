# Vgrid
Draws round-number price levels (psychological grid) above and below price, with Fibonacci levels (0.236–0.786) inside each zone and a highlighted 0.5 midpoint. Auto-sizes the grid for forex, gold, BTC, and futures (MNQ, MYM, ZB), redraws only when price enters a new zone, and is fully customizable.
### Vgrid — Psychological Price Grid + Fibonacci Zones

**What it does:**
Draws horizontal lines at round-number price levels (e.g. every 500 points on NQ, every 250 on gold) above and below the current price. Each zone between two round numbers is then split with Fibonacci levels (0.236, 0.382, 0.5, 0.618, 0.786), with the 0.5 midpoint styled separately so it stands out.

**Why I built it:**
Price tends to react at round numbers because that's where traders cluster orders, stops, and targets. Vgrid maps those levels automatically and adds Fib structure inside each zone, so I can see likely reaction points and midpoints without drawing anything by hand.

**Features:**
- **Auto grid sizing per instrument:** preset step sizes for major forex pairs (EURUSD, GBPUSD, USDJPY, etc.), gold, silver, BTC, and futures (MNQ, MYM, ZB). Root symbols match full contract names, so `MNQ` matches `MNQM2026`.
- **Manual override:** pick any step size from 0.005 to 10,000 points.
- **Self-updating:** the grid only redraws when price moves into a new zone, which keeps it lightweight.
- **Labels follow price:** level labels stay a set number of bars ahead of the current candle.
- **Fully customizable:** colors, line styles, widths, number of levels, and label visibility for the grid, the Fibs, and the 0.5 midpoint separately.

**Inputs:**
| Setting | Default | Description |
|---|---|---|
| Grid Step (Points) | 500 | Distance between round-number levels |
| Override Auto Grid | On | Use the manual step instead of per-instrument presets |
| Levels Above / Below | 15 / 15 | How many grid levels to draw on each side of price |
| Label Distance | 50 bars | How far right of the current bar labels appear |
| Show Fib Levels / Labels | On | Toggle Fibonacci levels inside each zone |
