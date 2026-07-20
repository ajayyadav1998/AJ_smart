# AJ Smart Indicator v0.2.3 — Developer Notes

## Why v0.2.2 Was Rejected

The v0.2.2 labels used `yloc.price` at a candle extreme, which is a price-coordinate placement rather than TradingView's candle-relative marker placement. Its four line handles were also explicitly deleted and reused for later trades, so historical trade drawings were intentionally lost.

## Why v0.2.3 Is More Robust

- BUY and SELL labels now use `yloc.belowbar` and `yloc.abovebar`. TradingView maintains these positions relative to their signal candles during zooming, scaling, panning, scrolling, and replay.
- Labels use `xloc.bar_index`, so they remain bound to the originating chart bar.
- Every confirmed trade creates four independent `line.new()` objects at its entry, stop loss, Target 1, and Target 2 prices.
- The script never retains, deletes, mutates, or recycles line handles. Each historical trade stays intact.
- The non-essential swing dots were removed to keep the chart focused on signals and trade levels.

## TradingView Object Limit

TradingView permits at most 500 line objects and 500 label objects for one script instance. The script requests those maximum limits. At four lines per trade, the chart can retain up to 125 complete historical trade level sets before the platform's line limit is reached.
