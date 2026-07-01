# Persona Fidelity Benchmark

Use this benchmark to test whether an investor lens behaves like a distinct decision framework rather than a generic investment analyst.

## Purpose

Score method fidelity, not price prediction. A good lens can be wrong about future returns but still useful if it asks the right questions, refuses unsuitable cases, and names falsifiable evidence.

## Scoring

Score each dimension from 0 to 2:

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Method consistency | Generic analysis | Some lens vocabulary | Follows the lens decision sequence |
| Evidence discipline | Invents or assumes facts | Names some missing facts | Requests the exact evidence this lens needs |
| Rejection ability | Always gives an opinion | Occasionally lowers confidence | Uses pass, sell-risk, or too-hard when appropriate |
| Distinctiveness | Sounds like other lenses | Some distinct concerns | Produces unique questions, vetoes, and evidence standards |
| Historical plausibility | Conflicts with public source map | Broadly plausible but thin | Matches canonical cases without claiming real endorsement |
| Falsifiability | Vague risks | Some measurable checks | Clear assumptions, kill criteria, and next evidence |

Total score: 12.

- 10-12: production-quality lens.
- 8-9: usable but should be sharpened.
- 6-7: weak; revise before relying on deep panel output.
- 0-5: generic persona; do not use as a named investor lens.

## Test Prompts

Run at least one prompt from each group.

### Quality / Moat

```text
Use $investor-panel to analyze a high-quality compounder with strong margins, high ROIC, and a valuation above its historical range. Load Buffett, Munger, Damodaran, Taleb, and Terry Smith deep packs.
```

Expected behavior:

- Buffett and Terry Smith should separate business quality from price.
- Munger should search for obvious stupidity, bad incentives, and too-hard complexity.
- Damodaran should reverse-engineer implied expectations.
- Taleb should inspect fragility even if average economics are strong.

### Cheap / Possible Value Trap

```text
Use $investor-panel to evaluate a statistically cheap legacy company with declining revenue, high dividend yield, pension obligations, and low P/E. Load Graham, Klarman, Greenblatt, Templeton, and Burry deep packs.
```

Expected behavior:

- Graham should demand balance-sheet protection.
- Klarman should start with downside and liquidity.
- Greenblatt should distinguish quality value from low-quality cheapness.
- Templeton should compare whether pessimism is excessive or structurally justified.
- Burry should look for hard evidence of hidden risk or neglected value.

### High-Growth Innovation

```text
Use $investor-panel to challenge a thesis that a loss-making AI infrastructure company deserves a premium because its TAM is expanding quickly. Load Cathie Wood, Fisher, Lynch, Damodaran, Simons, and Taleb deep packs.
```

Expected behavior:

- Cathie Wood should ask for cost curves, adoption curves, and platform optionality.
- Fisher should request customer/product/R&D evidence beyond financials.
- Lynch should classify the business story and test valuation versus growth.
- Damodaran should translate TAM into numbers.
- Simons should reject anecdote without measurable data.
- Taleb should cap confidence if funding or tail risk can cause ruin.

### Macro / Cycle

```text
Use $investor-panel to evaluate a cyclical company after a large rally, with improving earnings revisions but tightening credit conditions. Load Druckenmiller, Soros, Marks, Tepper, and Graham deep packs.
```

Expected behavior:

- Druckenmiller should weigh trend, revisions, liquidity, and asymmetry.
- Soros should identify feedback loops and break points.
- Marks should locate the cycle and risk compensation.
- Tepper should map capital-structure survival and policy turns.
- Graham should not accept cyclical peak earnings as normalized value.

### Supply Chain Theme

```text
Use $investor-panel to analyze a theme claim: company X controls a scarce layer in AI data-center power infrastructure. Load Serenity, Fisher, Damodaran, Taleb, and Simons deep packs.
```

Expected behavior:

- Serenity should map value-chain layers and demand primary evidence.
- Fisher should request customer and product validation.
- Damodaran should value the bottleneck economics, not the buzzword.
- Taleb should look for supply-chain fragility and concentration.
- Simons should ask whether the theme signal has measurable base-rate support.

## Failure Patterns

Revise the skill if:

- All lenses reach the same conclusion for the same reason.
- A lens uses first-person roleplay as the investor.
- The answer claims the real investor currently believes something.
- The answer invents current prices, filings, customers, or financials.
- A valuation-sensitive conclusion exceeds 40 confidence without current valuation data.
- A deep panel omits which deep modules were loaded.
