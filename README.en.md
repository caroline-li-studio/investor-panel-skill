# Investor Panel Skill

Investor Panel is a Codex / Agent Skill that puts one company in front of 26 distilled investor frameworks.

It is not one AI analyst giving one answer. It is an investment committee debate: Buffett on quality, Graham and Klarman on margin of safety, Damodaran on valuation, Taleb on tail risk, Druckenmiller and Soros on macro, Simons on statistical evidence, and Serenity on supply-chain bottlenecks.

The value is the disagreement. A company can be wonderful and overpriced, cheap and still a value trap, high-growth and fragile, or thematically attractive without evidence. Investor Panel is designed to surface those conflicts before producing a research-oriented synthesis.

It is not a data provider and it does not place trades. It consumes evidence from the user, web/search, filings, market-data tools, or a future data skill.

## What It Does

Investor Panel helps answer questions like:

- Is this company worth deeper research?
- What would Buffett, Munger, Graham, Damodaran, Taleb, and other lenses disagree about?
- Which stock in this candidate list deserves priority?
- What could break this thesis?
- Should a current holding be watched, trimmed, or reviewed for sell risk?
- Which supply-chain layer is actually scarce in a hot theme?

The skill is designed for evidence-backed research, not personality roleplay. It uses investor lenses as analytical frameworks and does not claim to represent the real opinions of any investor.

## Default Panel

Named investor and methodology lenses:

- Aswath Damodaran - narrative-to-numbers valuation
- Benjamin Graham - conservative value and margin of safety
- Bill Ackman - activist value creation and catalysts
- Cathie Wood - disruptive innovation and adoption curves
- Charlie Munger - inversion, incentives, and avoiding stupidity
- David Swensen - portfolio construction and institutional stewardship
- David Tepper - distressed value, capital structure, and crisis recovery
- George Soros - reflexivity, macro feedback loops, and regime shifts
- Howard Marks - market cycles, second-level thinking, and credit risk
- Jim Simons - statistical edge, robustness, and signal decay
- Joel Greenblatt - special situations and quality value
- John Templeton - global contrarian value and maximum pessimism
- Julian Robertson - Tiger-style long/short and relative winners
- Li Lu - quality value, long-term compounding, and China/Asia governance
- Michael Burry - contrarian and forensic downside analysis
- Mohnish Pabrai - Dhandho-style downside-first asymmetry
- Nassim Taleb - fragility, convexity, and tail risk
- Nick Sleep - scale economies shared and patient compounding
- Peter Lynch - understandable growth at a reasonable price
- Phil Fisher - long-term growth quality and scuttlebutt-style evidence
- Rakesh Jhunjhunwala - emerging-market compounding and cycles
- Seth Klarman - absolute-return value, distress, and margin of safety
- Stanley Druckenmiller - macro regime, liquidity, and asymmetric timing
- Terry Smith - high-quality compounding and disciplined inactivity
- Warren Buffett - durable moat, management, owner earnings, and margin of safety
- Serenity-style supply-chain lens - market story to system change to scarce layer

Specialist lenses:

- Fundamentals
- Valuation
- Technicals
- Growth
- News sentiment
- Market sentiment

## Supported Modes

- **Quick screen**: fast watch/pass/deep-dive recommendation.
- **Deep company analysis**: full panel vote and synthesis.
- **Candidate comparison**: rank several companies by research priority.
- **Thesis challenge**: attack a thesis and name falsifying evidence.
- **Hold/sell review**: evaluate sell-risk, opportunity cost, and monitoring triggers.
- **Theme or supply-chain scan**: rank scarce layers before ranking companies.

## Output Shape

A full panel review returns:

- Verdict
- Evidence Gate
- Consensus
- Disagreement
- Investor Votes
- Key Assumptions
- Risks & Kill Criteria
- Next Checks

The skill separates facts from assumptions and lowers confidence when evidence is missing, stale, or secondary.

## Example Prompts

```text
Use $investor-panel to analyze NVDA. Focus on whether the current valuation is supported by fundamentals and AI infrastructure demand.
```

```text
用 $investor-panel 比较 AAPL、MSFT、NVDA、TSLA，给我一个优先研究排序。
```

```text
Use $investor-panel to challenge this thesis: company X controls a scarce bottleneck in AI data-center power and the market is underpricing it.
```

```text
用 $investor-panel 做一个 hold/sell review：我持有这家公司，想知道什么情况说明我应该降低仓位。
```

## Installation

Copy the skill folder into a Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/investor-panel ~/.codex/skills/investor-panel
```

Or keep it inside a project and reference it as a project skill when your runtime supports project-local skills.

## Repository Layout

```text
skills/investor-panel/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── evidence-pack.md
    ├── investor-lenses.md
    ├── lens-creation.md
    ├── people-index.md
    ├── output-contract.md
    └── people/
        └── one deep profile per investor lens
```

## Boundaries

- Research support only.
- No guaranteed return language.
- No trade execution or order generation.
- No invented current prices, filings, financials, customers, contracts, ownership, or market caps.
- Current facts should be verified with available tools before high-confidence conclusions.

## Status

MVP skill implementation is complete and validates with the Codex skill validator.
