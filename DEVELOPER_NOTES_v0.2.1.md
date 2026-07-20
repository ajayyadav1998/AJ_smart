# AJ Smart Indicator v0.2.1 — Developer Notes

## Code Review Summary

The v0.2.1 release is a pure readability and maintainability refactor. The calculation order, directional formulas, user-input definitions, plot values, plot titles, plot settings, and alert contracts are preserved from v0.2.

## Refactored Sections

- Renamed candle, trend, swing, ATR, filter, and signal variables to describe their state and purpose.
- Renamed helper functions to distinguish value retrieval from action-oriented calculations.
- Clarified function contracts and section comments.
- Grouped comments around confirmation boundaries and compatibility-sensitive outputs.

## Performance Improvements

- No additional series calculations, loops, security requests, labels, or drawing objects were introduced.
- Existing intermediate values continue to be calculated once and reused by downstream filters and risk calculations.
- Direction-specific stop and target calculations remain separate intentionally, preserving the original arithmetic and avoiding unnecessary branch abstraction.

## Potential Future Improvements — Not Implemented

- Add automated visual/regression checks against a fixed set of historical symbols and timeframes.
- Introduce a dedicated state container when the planned trade state machine is added in a later feature release.
- Centralize styling constants only in a feature release that explicitly allows UI/input changes.
