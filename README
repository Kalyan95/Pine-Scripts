# Risk/Reward Calculator

## Inputs
- **margin** (default `100`): Capital allocated to open a position.
- **leverage** (default `1`): Multiplier applied to margin to determine overall exposure.
- **maint_margin_pct** (default `0.5`): Maintenance margin requirement expressed as a percentage; used to calculate liquidation price.
- **entry_price_input** (default `close`): Price at which the trade is entered. Defaults to the current closing price if left blank.
- **take_profit_input** (default `0`): Target price for taking profit. A value of `0` disables the take‑profit line.
- **stop_loss_input** (default `0`): Price for cutting losses. A value of `0` disables the stop‑loss line.

## Table Calculations
- **Position Size**: `margin * leverage / entry_price_input` — number of units in the position.
- **Risk**: `(entry_price_input - stop_loss_input) * position_size` — potential loss if stop loss is reached.
- **Reward**: `(take_profit_input - entry_price_input) * position_size` — potential gain if take profit is reached.
- **R/R Ratio**: `reward / risk` (absolute values) — ratio of potential reward to potential risk.
- **Liquidation Price**: `entry_price_input * (1 - (1 / leverage - maint_margin_pct))` — approximate price at which the position would be liquidated.
- **Margin Used**: equals the `margin` input.
- **Potential PnL**: displays risk and reward in account currency.
- **Risk % of Margin**: `risk / margin * 100`.

## Features and Description
- Customizable risk and reward lines with editable take‑profit and stop‑loss levels.
- Bottom‑right table summarizing position size, risk, reward, and key risk metrics.
- Visual and textual alerts when the liquidation price approaches the stop loss or falls below maintenance requirements.
- Designed for flexible position sizing and quick scenario analysis on any TradingView chart.

