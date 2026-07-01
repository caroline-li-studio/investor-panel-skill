# Deep Investor Profile Schema

Use this schema for deep Investor Panel persona packs. A deep pack is a distilled decision framework, not a biography and not a roleplay script.

## Files

Each investor directory should contain:

- `source-map.md`: primary-source targets, canonical cases, avoided sources, and citation rules.
- `framework.md`: core question, decision sequence, evidence needs, positive/negative patterns, and time horizon.
- `business-quality.md`: how the lens defines business quality, moat, industry fit, and customer economics.
- `management.md`: management, governance, incentives, capital allocation, and red flags.
- `financials.md`: financial metrics, accounting quality, cyclicality, and peer comparison discipline.
- `valuation.md`: valuation method, margin-of-safety standard, expectation test, and overpay risk.
- `risk-and-sell.md`: kill criteria, thesis-breaking facts, downside hierarchy, and hold/sell review.
- `eval-cases.md`: persona-fidelity cases and scoring rubrics.

## Required Output Behavior

When using a deep pack, produce:

- `Signal`: bullish, neutral, bearish, watch, pass, hold, sell-risk, or too-hard.
- `Confidence`: 0-100, capped by evidence quality.
- `Thesis`: one or two sentences in the lens's own decision logic.
- `Veto`: one fact that would make the lens reject or downgrade the idea.
- `Evidence needed`: facts required before confidence can rise.

## Guardrails

- Do not impersonate the investor or claim to know their current opinion.
- Do not quote long copyrighted passages. Paraphrase frameworks and cite source types.
- Do not turn famous quotes into the whole lens.
- Prefer primary sources over second-hand summaries.
- Always allow `too-hard` when the business, valuation, data, or timing is outside the lens's edge.
- Keep each lens distinct. If two profiles produce the same questions, revise one until it has a different evidence standard or veto path.

## Evidence Confidence Caps

- Cap confidence at 40 when current valuation is missing for a valuation-sensitive conclusion.
- Cap confidence at 50 when primary financials are missing.
- Cap confidence at 60 when the key claim rests only on secondary sources.
- Cap confidence at 70 when the business is clear but the valuation is approximate.
- Allow confidence above 80 only when primary evidence supports the critical assumptions and the lens has a clear reason to care.
