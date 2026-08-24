---
description: Interpret high- and low-volume nodes as evidence of past facilitation and rejection.
icon: chart-bar
---

# HVN / LVN

A **high-volume node (HVN)** is a price region with concentrated traded volume. It represents past facilitation and often supports rotation. A **low-volume node (LVN)** contains relatively little volume and often marks rejection or a zone through which price traveled efficiently.

## Expected behavior

Price commonly slows and rotates around an HVN because the market previously found agreement there. At an LVN, price may reject quickly or traverse rapidly toward the next HVN. These are tendencies conditioned on context.

Think in zones, not exact ticks. Bin size, profile period, and feed quality change the shape. A node visible on a weekly composite may matter more than one created by a short, low-liquidity session.

## Composite profiles

Profile a completed balance to locate its distribution. Multiple HVNs separated by an LVN form a double distribution: acceptance through the separator can rotate toward the other distribution's HVN; rejection can return price to the origin node.

## Decision sequence

1. Identify the profile that generated the node.
2. Determine whether price approaches from balance or imbalance.
3. Observe speed, volume, and response at the zone.
4. Require acceptance or rejection before choosing rotation or continuation.

{% hint style="info" %}
An HVN does not inherently support price, and an LVN is not inherently resistance. Direction of approach and current participation decide the response.
{% endhint %}

**Drill:** Select ten completed balances. Mark their major nodes, then study the first future revisit without moving the profile anchors.
