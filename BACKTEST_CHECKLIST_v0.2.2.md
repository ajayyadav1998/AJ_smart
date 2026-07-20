# AJ Smart Indicator v0.2.2 — Backtest Checklist

- [ ] Verify v0.2.1 and v0.2.2 generate BUY signals on identical bars.
- [ ] Verify v0.2.1 and v0.2.2 generate SELL signals on identical bars.
- [ ] Verify each BUY label reads `▲ BUY` and is anchored below its signal candle.
- [ ] Verify each SELL label reads `▼ SELL` and is anchored above its signal candle.
- [ ] Verify historical BUY/SELL labels persist after later signals.
- [ ] Verify only four active level lines exist after each new signal.
- [ ] Verify the active Entry, Stop Loss, Target 1, and Target 2 lines retain their setup prices while new bars arrive.
- [ ] Verify level lines are deleted and recreated on the next confirmed setup.
- [ ] Verify labels and lines remain aligned during zooming, panning, and scrolling.
- [ ] Verify existing alert titles and messages remain unchanged.
