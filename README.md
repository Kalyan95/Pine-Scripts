# Leverage Trading Calculator

This TradingView indicator helps evaluate a leveraged trade by computing position size, potential risk and reward, and an approximate liquidation price.

## User Inputs
- **Margin** – funds dedicated to the trade
- **Leverage** – multiple applied to the margin
- **Entry Price** – price at which the position is opened
- **Stop Loss** – price that exits the trade if hit
- **Take Profit** – price to capture gains

## Calculations
- **Position size:** `margin * leverage`
- **Risk and reward:** price difference between entry and stop/take multiplied by position size and normalized by entry price
- **Risk‑reward ratio:** `reward / risk`
- **Liquidation price:** `entry * (1 ± 1/leverage)` for isolated margin (minus for long, plus for short)

## Long/Short Orientation and Safety
The script determines orientation from the stop-loss:
- If `stop < entry` the position is long, otherwise it is short.
- A stop on the wrong side of the liquidation price is flagged as unsafe.

## Table and Alerts
A table prints the computed values – position size, risk, reward, risk‑reward ratio, liquidation price, and direction. Alerts notify when a stop is unsafe or when a long/short setup is present.
