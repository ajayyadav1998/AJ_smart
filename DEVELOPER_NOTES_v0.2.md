# AJ Smart Indicator v0.2 — Developer Notes

- This is an indicator, not a backtest strategy. It intentionally does not manage positions or calculate performance.
- A swing marker appears only on the candle where its pivot becomes confirmed; no historical marker is back-painted. Trade logic uses confirmed pivots only.
- The hybrid stop uses the farther valid protective level: ATR stop versus swing level plus/minus the configured ATR buffer.
- A newly confirmed setup replaces the currently displayed setup levels. Trade lifecycle management and risk-reward boxes are reserved for v0.3.
- The script uses original logic and does not reproduce a third-party indicator.
- Recommended validation symbols: NIFTY, BANKNIFTY, and their relevant option contracts on 5m, 15m, and 30m charts.
