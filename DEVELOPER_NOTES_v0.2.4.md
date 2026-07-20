# AJ Smart Indicator v0.2.4 — Stabilization Notes

## Root Cause Analysis

v0.2.3 created four new `line.new()` objects for every confirmed trade while retaining all existing lines. Since every historical setup remained, each chart accumulated four more lines per trade and rapidly became unreadable.

## What Changed

- Four `var line` IDs retain the Entry, Stop Loss, Target 1, and Target 2 lines of the active trade.
- Before creating lines for a new confirmed BUY or SELL setup, the script deletes each existing active-trade line by ID.
- It then creates a new independent line for each of the four calculated prices.
- BUY and SELL labels use `xloc.bar_index` plus `yloc.belowbar` / `yloc.abovebar`; no ATR or price offsets are used.
- Swing dots and other temporary drawings are absent.

## Why This Is Stable

The script can hold no more than four trade-level line objects because the prior set is deterministically deleted before replacement. `extend.right` keeps each level at the exact creation price without updating it on later bars. Labels are created only inside the existing confirmed BUY/SELL signal branches, yielding one label for each confirmed signal bar.
