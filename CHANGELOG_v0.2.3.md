# AJ Smart Indicator — Changelog

## v0.2.3 — 18 July 2026

- Replaced price-anchored BUY/SELL labels with TradingView candle-relative labels (`yloc.belowbar` / `yloc.abovebar`).
- Removed optional swing-marker dots and their display input.
- Replaced the single active-trade line lifecycle with four independent line objects per confirmed trade.
- Historical trade-level lines are no longer deleted or recycled by the script.
- Preserved all signal conditions, EMA/ATR/risk calculations, and alert contracts.
