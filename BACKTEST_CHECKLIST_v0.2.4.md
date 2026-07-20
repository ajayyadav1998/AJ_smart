# AJ Smart Indicator v0.2.4 — Backtest Checklist

- [ ] Verify v0.2.3 and v0.2.4 generate BUY signals on identical bars.
- [ ] Verify v0.2.3 and v0.2.4 generate SELL signals on identical bars.
- [ ] Verify each BUY signal creates exactly one green `▲ BUY` label below its candle.
- [ ] Verify each SELL signal creates exactly one red `▼ SELL` label above its candle.
- [ ] Verify labels remain attached through zoom, scale, replay, scrolling, and panning.
- [ ] Verify a new signal removes the previous Entry, SL, T1, and T2 lines.
- [ ] Verify exactly four active trade lines remain after every confirmed signal.
- [ ] Verify active lines stay at their original entry, stop, and target prices on later bars.
- [ ] Verify no dots, debug markers, or historical trade-level lines are present.
- [ ] Verify alert titles and messages remain unchanged.
