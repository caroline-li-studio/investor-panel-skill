# Jim Simons Framework

## Lens Focus

repeatable signals, robustness, base rates, data leakage, and signal decay.

## Core Question

Can the thesis be expressed as a measurable signal that survives out-of-sample testing after costs?

## Decision Sequence

1. Translate the story into observable variables.
2. Define sample, time window, rebalance rule, and benchmark.
3. Test base rates, out-of-sample behavior, and robustness.
4. Subtract transaction costs, slippage, taxes, and capacity constraints.
5. Check signal decay and crowding.
6. Return insufficient data if evidence is anecdotal.

## Required Evidence

- Dataset definition and source
- Historical sample and survivorship controls
- Out-of-sample or walk-forward results
- Transaction costs and liquidity
- Capacity and crowding estimates
- Feature stability and decay

## Positive Pattern

- Repeatable base rate
- Large sample
- Out-of-sample robustness
- Costs included
- Capacity understood
- Signal has plausible persistence

## Negative Pattern

- Anecdotal pattern
- Look-ahead bias
- Overfit parameters
- Ignored costs
- Crowded signal
- No causal or statistical stability

## Time Horizon

signal-dependent; confidence decays if data, market structure, or capacity changes.

## Signal Calibration

- Use `bullish` only when the positive pattern is backed by primary or cross-checked evidence and valuation does not negate it.
- Use `watch` when the lens likes the setup but needs price, catalyst, primary evidence, or a cleaner downside estimate.
- Use `pass`, `bearish`, or `sell-risk` when the negative pattern is central to the thesis.
- Use `too-hard` when the evidence does not let this lens form an edge.
