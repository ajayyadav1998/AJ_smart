# AJ Smart Indicator — Changelog

## v0.2.2 — 18 July 2026

- Replaced BUY and SELL `plotshape()` markers with permanent `label.new()` objects.
- Replaced Entry, Stop Loss, Target 1, and Target 2 `plot()` series with four persistent `line.new()` objects.
- New setup deletes and replaces only the previous four active trade-level lines.
- Preserved all signal conditions, risk calculations, trend and ATR calculations, input definitions, and alert contracts.
