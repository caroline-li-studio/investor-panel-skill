# Prompt Test Suite

Use these prompts as regression tests after changing Investor Panel. They are designed to check mode routing, evidence discipline, deep-pack loading, and panel disagreement.

## Test 1: Single-Stock Deep Dive With Provided Facts

```text
Use $investor-panel to run a deep company analysis on Company A.

Facts:
- Enterprise software company with 90% recurring revenue.
- Revenue grew 24%, 21%, and 18% in the last three years.
- Gross margin is 78%, operating margin is 14%, FCF margin is 21%.
- Net cash balance sheet.
- Current EV/revenue is 14x and FCF yield is 2.1%.
- Customer retention is strong but sales cycles are lengthening.

Load Buffett, Munger, Damodaran, Terry Smith, Cathie Wood, Taleb, and Simons deep packs.
```

Expected:

- Uses Deep Panel Evidence Mode.
- Lists loaded deep packs/modules.
- Separates business quality from valuation.
- Caps confidence if current filing dates or price dates are not supplied.

## Test 2: Single-Stock Deep Dive With Missing Facts

```text
Use $investor-panel to analyze Company B, an AI infrastructure supplier. I only know it is mentioned often in AI data-center discussions.
```

Expected:

- Does not invent revenue, market cap, customers, contracts, or current valuation.
- Uses a low-confidence quick or provisional view.
- Serenity asks for value-chain role, customer certification, capacity, and primary evidence.
- Output emphasizes Evidence Gaps and Next Checks.

## Test 3: Multi-Company Comparison

```text
Use $investor-panel to compare AAPL, MSFT, NVDA, and TSLA by research priority.
Focus on where Buffett, Damodaran, Druckenmiller, Taleb, Cathie Wood, and Simons would disagree.
```

Expected:

- Uses Candidate Comparison format.
- Ranks research priority, not guaranteed returns.
- Does not invent current prices or financials without tools.
- Produces distinct disagreements rather than one blended answer.

## Test 4: Serenity-Style Theme Scan

```text
Use $investor-panel for a theme scan: AI data-center power infrastructure.
First map scarce supply-chain layers, then name what evidence I need before researching companies.
```

Expected:

- Starts with value-chain layer priority before company ranking.
- Serenity lens leads the workflow.
- Identifies scarce-layer evidence: supplier count, qualification time, capacity expansion, certification, lead times, and standards.
- Passes finalists to valuation and risk lenses only after evidence quality is clear.

## Test 5: Thesis Challenge

```text
Use $investor-panel to challenge this thesis:
Company C is a buy because it has a dominant AI narrative, high revenue growth, and every competitor will need to use its platform.
```

Expected:

- Uses Thesis Challenge format.
- Damodaran converts narrative to revenue/margin/reinvestment assumptions.
- Simons asks for measurable evidence and base rates.
- Taleb identifies fragility, leverage, customer concentration, or model risk.
- Munger checks incentives and hype.

## Test 6: Hold / Sell Review

```text
Use $investor-panel for a hold/sell review.
I own Company D after a 5x move. It still has high ROIC and fast growth, but valuation is now far above peers and insiders have started selling.
```

Expected:

- Uses Hold / Sell Review format.
- Checks sell criteria: price far above value, moat deterioration, management/incentive problem, opportunity cost, tail risk.
- Buffett/Terry Smith can still like quality while Damodaran or Klarman flags valuation.
- Output gives monitoring triggers and kill criteria.

## Test 7: Persona Fidelity Spot Check

```text
Use $investor-panel to analyze a statistically cheap company with declining revenue, high debt, and low P/E.
Only load Graham, Klarman, Greenblatt, Templeton, and Burry deep packs.
```

Expected:

- Graham focuses on asset protection and earnings stability.
- Klarman starts with downside and cash optionality.
- Greenblatt checks return on capital and special-situation mechanics.
- Templeton asks whether pessimism is excessive or structurally justified.
- Burry looks for hard filing evidence and hidden risk.
- The lenses should not all produce the same reason.

## General Pass Criteria

- No first-person investor roleplay.
- No claim that the real investor currently endorses the output.
- No invented current facts.
- Confidence is capped when key evidence is missing.
- At least one output uses `too-hard`, `watch`, or `provisional` when evidence is insufficient.
