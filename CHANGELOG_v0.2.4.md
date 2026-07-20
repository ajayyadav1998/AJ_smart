# AJ Smart Indicator — Changelog

## v0.2.4 Stabilization Release — 18 July 2026

- Restored a strict single-active-trade lifecycle for Entry, Stop Loss, Target 1, and Target 2 lines.
- Added persistent `var line` IDs for the four active trade levels.
- Deletes the prior four lines before creating a new confirmed BUY or SELL trade set.
- Retained TradingView candle-relative BUY/SELL marker placement.
- Preserved all signal logic, EMA/ATR/risk calculations, inputs, and alert contracts.
