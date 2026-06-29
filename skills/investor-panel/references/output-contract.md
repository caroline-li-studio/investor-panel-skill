# Output Contract

Use concise, evidence-backed outputs. Prefer tables for panel votes and comparisons. Keep assumptions separate from facts.

## Standard Full Panel

```markdown
## Verdict
[Research verdict: Buy/Watch/Pass/Hold/Sell-risk/Too hard] - [one-sentence rationale]

## Evidence Gate
- Evidence quality: [Strong/Medium/Weak]
- Currentness: [latest filing/date/price date if known]
- Main gaps: [missing facts that limit confidence]

## Consensus
[2-4 bullets where the panel agrees]

## Disagreement
[2-4 bullets where the lenses conflict]

## Investor Votes
| Lens | Signal | Confidence | Core reason | Veto / kill criterion |
|---|---:|---:|---|---|

## Key Assumptions
1. [Falsifiable assumption]
2. [Falsifiable assumption]
3. [Falsifiable assumption]

## Risks & Kill Criteria
- [Risk]: [what would prove it is worsening]
- [Risk]: [what would prove it is worsening]

## Next Checks
- [filing/metric/source/event to verify]
- [filing/metric/source/event to verify]
```

For full panels, include named investor lenses first, then specialist lenses only when they add material evidence. If the table gets long, keep each reason to one sentence and move detail into `Consensus`, `Disagreement`, or `Risks & Kill Criteria`.

## Quick Screen

Use this when the user wants a fast answer or evidence is light.

```markdown
## Quick Verdict
[Deep dive / Watch / Pass / Too hard] - [one sentence]

## Why
- [Business quality or theme logic]
- [Valuation or evidence issue]
- [Main risk]

## Panel Snapshot
| Lens | Lean | Reason |
|---|---|---|

## Need Before Confidence
- [missing fact]
- [missing fact]
```

## Candidate Comparison

Use this when comparing companies.

```markdown
## Ranking
| Rank | Company | Research priority | Best supporting lens | Main concern |
|---:|---|---|---|---|

## Why This Order
[Short explanation of the tradeoff: quality, price, growth, macro, tail risk, scarce-layer control.]

## Company Notes
| Company | Bull case | Bear case | Evidence gap | Next check |
|---|---|---|---|---|
```

## Thesis Challenge

Use this when the user gives a thesis to attack.

```markdown
## Challenge Verdict
[Robust / Plausible but unproven / Fragile / Too hard] - [one sentence]

## Thesis Assumptions
| Assumption | Evidence status | What would disprove it |
|---|---|---|

## Strongest Objections
1. [Objection]
2. [Objection]
3. [Objection]

## What Would Change My Mind
- [specific evidence]
- [specific evidence]
```

## Hold / Sell Review

Use this when the user owns or is considering trimming/selling.

```markdown
## Hold/Sell Verdict
[Hold / Trim-risk / Sell-risk / Too hard] - [one sentence]

## Sell Criteria
| Criterion | Status | Evidence |
|---|---|---|
| Price far above value | [Yes/No/Unknown] | |
| Moat deterioration | [Yes/No/Unknown] | |
| Management/incentive problem | [Yes/No/Unknown] | |
| Better opportunity cost | [Yes/No/Unknown] | |
| Tail-risk or ruin risk | [Yes/No/Unknown] | |

## Monitoring Triggers
- [metric/event that would upgrade]
- [metric/event that would downgrade]
```

## Theme / Supply-Chain Scan

Use this when the request is about a sector, theme, or market opportunity.

```markdown
## Layer Priority
Start with the layers: [layer 1], [layer 2], [layer 3]. The best research path is to find who controls the hard-to-scale parts.

| Layer | Scarcity reason | Evidence quality | Companies to inspect |
|---|---|---|---|

## Candidate Priority
| Rank | Company | Market | Chain position | Why it ranks here | Main risk |
|---:|---|---|---|---|---|

## What Could Be Wrong
- [failure condition]
- [failure condition]

## Next Research Move
- [source/filing/metric/customer check]
```

## Style Rules

- Lead with judgment.
- Use the user's language.
- Keep investor lenses distinct.
- Say "provisional" when evidence is thin.
- Do not bury missing evidence at the end.
- Do not present direct orders or guaranteed outcomes.
