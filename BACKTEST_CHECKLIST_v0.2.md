# AJ Smart Indicator v0.2 — Backtest Checklist

- [ ] Test NIFTY and BANKNIFTY across 5m, 15m, and 30m timeframes.
- [ ] Confirm each marker appears only after its candle closes.
- [ ] Confirm swing-derived stops use only already-confirmed pivots.
- [ ] Check long stop is below entry and short stop is above entry.
- [ ] Check Target 1 and Target 2 remain on the correct side of entry.
- [ ] Compare default and adjusted ATR settings in high- and low-volatility sessions.
- [ ] Record setup count, win rate, average R outcome, maximum adverse excursion, and slippage assumptions.
- [ ] Exclude illiquid option strikes and document the strike-selection rule used.
- [ ] Test alerts with “Once Per Bar Close”.
- [ ] Validate results separately for trend, range, gap, and event-driven sessions.
