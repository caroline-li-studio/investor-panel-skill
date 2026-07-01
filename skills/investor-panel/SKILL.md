---
name: investor-panel
description: Multi-investor research panel for company, stock, and investment thesis analysis. Use when an AI agent should evaluate a public company, private business, stock idea, watchlist, holding, sell decision, or investment thesis through multiple investor frameworks such as Buffett, Munger, Graham, Lynch, Fisher, Damodaran, Ackman, Cathie Wood, Michael Burry, Pabrai, Druckenmiller, Taleb, Jim Simons, Joel Greenblatt, Seth Klarman, Howard Marks, George Soros, David Tepper, John Templeton, Li Lu, Nick Sleep, Terry Smith, David Swensen, Julian Robertson, Rakesh Jhunjhunwala, and Serenity-style supply-chain research. Trigger on requests like "use Investor Panel", "investment panel", "investor panel", "投资大师 panel", "智囊团", "让 Buffett/Munger/Taleb/Serenity 一起看", "compare these stocks", "challenge this thesis", "hold or sell", "is this worth deeper research", or any request for a structured multi-perspective investment judgment. Research support only; no trade execution or guaranteed-return language.
---

# Investor Panel

Use Investor Panel as a research committee, not as a single persona. The job is to gather or inspect evidence, run distinct investor lenses, surface disagreement, and synthesize a research decision with clear assumptions and kill criteria.

Keep the skill data-source agnostic. Use whatever evidence is available from the user, local files, filings, web/search, market-data tools, or a future data skill. Do not assume Financial Datasets, a-stock-data, OpenBB, or any provider is present.

## Request Router

Classify the request before analysis:

- **Quick screen**: User asks whether a company or stock is worth deeper work. Use a compact panel and return watch/pass/deep dive.
- **Deep company analysis**: User asks for a full company or ticker review. Run the full panel workflow.
- **Candidate comparison**: User provides several companies. Rank research priority and explain the tradeoffs.
- **Thesis challenge**: User provides a thesis. Attack the assumptions and name evidence that would disprove it.
- **Hold/sell review**: User owns or tracks a position. Check sell criteria, downside, opportunity cost, and monitoring triggers.
- **Theme or supply-chain scan**: User asks about a sector/theme. Use the Serenity lens first to rank scarce layers, then apply company-level lenses to candidates.

## Evidence Gate

Start by deciding whether the answer depends on current facts. For current prices, filings, earnings, management changes, news, regulation, estimates, or "now/latest/today/current/最近/现在", use available tools before giving a high-confidence conclusion.

If evidence is missing, continue only at the appropriate confidence level:

- **Enough for quick screen**: business model, rough valuation, and obvious risks.
- **Enough for deep analysis**: read or obtain the evidence pack in `references/evidence-pack.md`.
- **Not enough**: state the missing facts under `Evidence Gaps` and give only a provisional view.

Never invent current prices, financials, filings, customers, contracts, ownership, or market caps. Mark uncertain data as an assumption.

## Panel Protocol

For a full analysis:

1. **Frame the case**: company, market, time horizon, user objective, and available evidence.
2. **Run the lenses**: read `references/investor-lenses.md` and produce one distinct vote per relevant investor.
3. **Deepen when needed**: for named-investor requests, deep dives, thesis challenges, hold/sell reviews, or thin short-lens reasoning, read `references/people-index.md`, the relevant compact `references/people/*.md` profile, and the relevant deep pack modules under `references/people/deep/<investor>/`.
4. **Debate the contradictions**: identify conflicts among quality, price, growth, macro, tail risk, and supply-chain evidence.
5. **Synthesize**: read `references/output-contract.md` and produce the matching output mode.
6. **Name falsifiers**: give kill criteria and next checks that would change the conclusion.

For quick screens, use only the most relevant lenses and keep the answer short. For theme scans, rank value-chain layers before ranking companies.

## Deep Pack Loading Protocol

Use progressive disclosure:

- **Quick screen**: read `references/investor-lenses.md`; read compact profiles only for named lenses.
- **Standard deep company analysis**: read `references/people-index.md` plus compact profiles for all materially relevant investors; load deep modules only for the 5-9 lenses driving the conclusion or disagreement.
- **Named investor request**: load that investor's `source-map.md`, `framework.md`, and whichever of `business-quality.md`, `management.md`, `financials.md`, `valuation.md`, or `risk-and-sell.md` matches the user question.
- **Thesis challenge or hold/sell review**: load `risk-and-sell.md` and `eval-cases.md` for the named or most relevant lenses.
- **Persona quality or lens creation work**: load `references/people/deep/PROFILE_SCHEMA.md` and `references/lens-creation.md`.
- **Skill evaluation or regression testing**: load `references/evals/persona-fidelity-benchmark.md`, `references/evals/panel-debate-benchmark.md`, and `references/evals/prompt-test-suite.md`.

When a deep pack is loaded, the lens must output `Signal`, `Confidence`, `Thesis`, `Veto`, and `Evidence needed`. If a deep module is not loaded, do not pretend to have used it.

## Default Roster

Use these lenses unless the user requests a subset:

- Aswath Damodaran: narrative-to-numbers valuation, DCF assumptions, uncertainty ranges.
- Benjamin Graham: balance sheet protection, conservative valuation, margin of safety, net-net instincts.
- Bill Ackman: activist value creation, governance, strategic change, catalyst path.
- Cathie Wood: disruptive innovation, exponential growth, adoption curves, optionality.
- Charlie Munger: inversion, incentives, cognitive errors, quality at fair price, too-hard pile.
- David Swensen: portfolio role, asset allocation, governance, liquidity, long-term stewardship.
- David Tepper: distressed value, capital structure survival, policy turns, crisis recovery.
- George Soros: reflexivity, macro feedback loops, regime shifts, positioning.
- Howard Marks: market cycles, second-level thinking, credit risk, offense versus defense.
- Jim Simons: statistical edge, base rates, robustness, signal decay, capacity limits.
- Joel Greenblatt: special situations, quality value, earnings yield, return on capital.
- John Templeton: global contrarian value, maximum pessimism, cross-market comparison.
- Julian Robertson: Tiger-style long/short, management quality, relative winners and losers.
- Li Lu: quality value, long-term compounding, China/Asia governance and policy risk.
- Michael Burry: contrarian deep value, hidden risks, short theses, forensic skepticism.
- Mohnish Pabrai: low-risk high-uncertainty bets, cloning, downside-first Dhandho logic.
- Nassim Taleb: fragility, leverage, convexity, tail risk, ruin avoidance.
- Nick Sleep: scale economies shared, customer value flywheels, owner-oriented compounding.
- Peter Lynch: understandable business, growth at reasonable price, unit-level story, PEG discipline.
- Phil Fisher: long-term growth quality, R&D, management depth, customer/scuttlebutt evidence.
- Rakesh Jhunjhunwala: emerging-market growth, domestic demand, cyclicality, management conviction.
- Seth Klarman: absolute-return value, margin of safety, distress, cash optionality.
- Stanley Druckenmiller: macro/liquidity regime, trend, asymmetric setup, risk/reward timing.
- Terry Smith: high-quality compounding, ROIC, cash conversion, disciplined inactivity.
- Warren Buffett: business quality, moat, management, owner earnings, margin of safety.
- Serenity: market story to system change to scarce supply-chain layer to evidence.
- Specialist lenses when useful: fundamentals, valuation, technicals, growth, news sentiment, market sentiment.

## Output Rules

Use the user's language. Chinese prompts should receive Chinese answers unless the user asks otherwise.

Do not roleplay as a living or deceased investor. Say "Buffett lens" or "Munger lens", not "I am Buffett." Avoid pretending these are the investors' actual opinions.

Keep direct trading responsibility with the user. Use research framing such as "research verdict", "priority", "watch", "pass", "hold review", or "sell-risk flag". Avoid guaranteed return language and do not generate orders.

## Bundled Resources

Load only what is needed:

- `references/investor-lenses.md`: concise rules for each investor framework.
- `references/lens-creation.md`: method for adding or revising investor lenses.
- `references/people-index.md`: map from investor names to compact profiles and deep packs.
- `references/people/*.md`: compact distilled profiles for each named investor or methodology lens.
- `references/people/deep/PROFILE_SCHEMA.md`: schema and quality bar for deep investor profile packs.
- `references/people/deep/<investor>/*.md`: source-backed deep modules for framework, evidence standards, valuation, risks, and eval cases.
- `references/evals/persona-fidelity-benchmark.md`: rubric for checking whether a lens behaves like a distinct decision framework.
- `references/evals/panel-debate-benchmark.md`: rubric for checking whether the panel creates useful disagreement and next checks.
- `references/evals/prompt-test-suite.md`: prompt-level regression cases covering deep dive, comparison, theme scan, thesis challenge, hold/sell review, and missing evidence.
- `references/evidence-pack.md`: evidence checklist and normalized company packet.
- `references/output-contract.md`: output formats for quick screen, deep dive, comparison, thesis challenge, hold/sell review, and theme scan.
