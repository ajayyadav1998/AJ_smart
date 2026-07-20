# AJ Smart Indicator v0.2.2 — Developer Notes

## Why the Previous Drawing Failed

`plotshape()` and `plot()` are bar-series renderers. They do not create independent chart objects that retain a trade's exact creation state. The plotted level series therefore follows its current series value instead of existing as a dedicated, fixed trade drawing.

## What Changed

BUY and SELL markers are now independent `label.new()` objects, anchored by `xloc.bar_index` and the signal candle's low/high price. Each is created on the confirmed signal bar and is never deleted by the script.

Entry, Stop Loss, Target 1, and Target 2 are now four `line.new()` objects. A new confirmed setup deletes only the prior four active level lines, then creates a new fixed-price set that extends right.

## How the New Drawing System Works

- Signal labels are intentionally not assigned to reusable variables, so later setups cannot delete them.
- Active level-line handles are retained in `var line` variables and are deleted only when a replacement setup is created.
- Every level line uses `xloc.bar_index`, the signal candle's `bar_index`, and its calculated candle-price level.
- `extend.right` continues each line without changing its original price.
- TradingView limits any script to a maximum of 500 labels; the script requests that maximum and performs no label deletion.
