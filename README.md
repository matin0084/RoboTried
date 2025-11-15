## RoboTried
########Three-Candle Channel Trading EA (MQL5)

This Expert Advisor is based on a three-candle channel pattern combined with Moving Average filtering.
The EA analyzes market structure on the selected timeframe and places Buy Limit or Sell Limit orders when both channel direction and MA conditions are confirmed.


---

📈 Strategy Overview

1. Three-Candle Channel Pattern

The EA checks whether the last 3 candles form a valid bullish or bearish channel:

Bullish Channel:
Each candle’s high and low is higher than the previous one.

Bearish Channel:
Each candle’s high and low is lower than the previous one.

Additional BO (Break-Out) confirmation is applied.


#2. Moving Average Filter

The EA verifies that the last 3 candles are:

Above the MA → for Buy setups

Below the MA → for Sell setups


The MA period, method, and applied price are user-configurable.


---

##📌 Entry Logic

When conditions align:

BUY LIMIT is placed at previous candle low.

SELL LIMIT is placed at previous candle high.

Stop Loss is automatically set based on candle structure.

Take Profit is calculated using a configurable Reward Ratio.



---

##⚙️ Inputs

Parameter	Description

MaPeriod	Moving Average period
MaMethod	MA method (SMA, EMA, etc.)
MaPrice	Applied price
timeframe	Timeframe selection (M1, M5, M15, M30, H1)
Reward	Risk/Reward multiplier
LimitTime	Max waiting time before deleting orders



---

##📌 Money Management

Lot size is automatically calculated using the distance between entry and stop loss.


---

##🔧 Additional Features

Auto-deletes pending orders if price does not activate them within LimitTime.

Uses the modern CTrade library for execution.

Clean modular functions for checking channel, MA, BO, and lot size.



---

#📜 Disclaimer

This EA is provided for educational purposes.
Backtest and forward-test before using it on a live account.
Trading forex involves financial risk.
