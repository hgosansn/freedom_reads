---
description: Select an entry trigger that balances confirmation, price, and information risk.
icon: crosshairs
---

# Entry

An entry is the moment sufficient evidence exists to take defined risk. It is not the thesis itself. A consistent entry model makes setup statistics interpretable.

## Three entry styles

| Style | Advantage | Cost |
|---|---|---|
| Anticipation at location | Best price, smallest stop | Least confirmation, more false starts |
| Confirmation on displacement | More information | Worse price, larger stop |
| Retest after confirmation | Balance of price and evidence | Retest may never occur |

Choose one primary style per setup. Mixing them during a trade usually means chasing after the planned entry is missed.

## Trigger specification

Define instrument, venue, trigger timeframe, observable event, permitted order type, maximum slippage, and cancellation condition. “Enter on strength” is not testable; “enter on the first five-minute close above the reclaim candle, provided distance to invalidation remains below 0.6%” is.

Limit orders control price but risk no fill. Market orders prioritize execution but expose the trade to spread and slippage. Stop-market orders confirm movement but may fill poorly during liquidations. Match the order to liquidity and urgency.

{% hint style="danger" %}
Never increase size merely because a delayed entry makes the stop farther away. Position size is derived from fixed risk divided by stop distance.
{% endhint %}

**Drill:** Replay 30 instances of one setup and compare all three entry styles using realistic fees and slippage. Select by expectancy, not win rate alone.
