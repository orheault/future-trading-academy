# Week 2 — Coach Review

## Part A — First submission, reviewed 2026-09-15

**Evidence:** Answers to questions 1–8 in `ASSIGNMENT.md`.
**Current status:** Parts A and B validated; proceed to Part C. Earlier review entries below preserve the correction history.
**Assessment scope:** Part A only. No overall weekly score or pass assigned.

The table below records the first submission. The student subsequently revised answers in place; the follow-up review below distinguishes those revisions from the original assessment.

| Question | Assessment | Feedback |
|---:|---|---|
| 1 | Correct | MES: $5/point × 0.25 points/tick = $1.25/tick per contract. Dividing by four is equivalent here. |
| 2 | Correct | 3.75 / 0.25 = 15 ticks; 15 × $1.25 = $18.75. Your decomposition also works. |
| 3 | Correct | MNQ: $2/point × 0.25 points/tick = $0.50/tick; 14 ticks = $7. |
| 4 | Correct results, incorrect formula | MGC: multiply 10 oz by $0.10/oz to obtain $1 per tick. The written 10 / 0.1 equals 100, not 1. The 23-tick move and $23 result are correct. |
| 5 | Incorrect tick-value derivation; correct final move result | MCL: 100 barrels × $0.01/barrel = $1 per tick. Dividing 100 by 0.01 does not produce a dollar tick value. A $0.27/barrel move is 27 ticks and $27 per contract. |
| 6 | Correct | MES $30,000; MNQ $40,000; MGC $25,000; MCL $7,500. |
| 7 | Correct unchanged values; explanation needs precision | Before and after: $30,000 notional and $1.25 per tick in magnitude. The required margin increases by $500. The exchange defines the multiplier; notional also depends on the futures price and quantity. Clearing requirements and broker policies both matter for margin; in this hypothetical, the broker changes its requirement. |
| 8 | Correct reasoning | Explicitly state both adjacent valid prices: 6,000.00 and 6,000.25. The proposed 6,000.10 price is invalid on this grid. |

## Main distinction to retain

```text
Dollar tick value = contract unit/multiplier × tick size
Number of ticks in a move = price movement ÷ tick size
```

For commodities, the units make this clear:

```text
MGC: 10 oz/contract × $0.10/oz per tick = $1/contract per tick
MCL: 100 barrels/contract × $0.01/barrel per tick = $1/contract per tick
```

Specifications and references are in `notes/contract-math.md`. Margin distinction: [CME margin lesson](https://www.cmegroup.com/education/courses/introduction-to-futures/margin-know-what-is-needed).

## Required follow-up before validating Part A

1. Revise the formulas in questions 4 and 5, retaining the original attempts.
2. Clarify question 7 and explicitly list both grid prices in question 8.
3. Complete these new questions without copying the worked corrections. Show units:
   - One MGC moves by $1.70/oz. Derive its tick value, then calculate ticks and dollar movement.
   - One MCL moves by $0.34/barrel. Derive its tick value, then calculate ticks and dollar movement.

Questions 4 and 5 are safety-critical. Correct final numbers with an invalid derivation do not yet meet the mastery requirement. Review the new attempts before marking Part A validated and proceeding with the next reviewed block.

## Part A — Follow-up review, 2026-09-15

Both new calculations submitted in the conversation are correct:

- MGC: 10 oz × $0.10/oz = $1 per tick; $1.70/oz ÷ $0.10/oz per tick = 17 ticks; movement value = $17 per contract.
- MCL: 100 barrels × $0.01/barrel = $1 per tick; $0.34/barrel ÷ $0.01/barrel per tick = 34 ticks; movement value = $34 per contract.

The assignment now correctly multiplies to derive tick value in questions 4 and 5. Question 7's explanation has been clarified. Question 8 identifies the correct neighboring levels in prose.

One notation issue remains in the revised question 5: `$0.27/barrel × 100 barrels` yields **$27**, not **27 ticks**. Write the tick conversion separately as `$0.27/barrel ÷ $0.01/barrel per tick = 27 ticks`, then `27 ticks × $1/tick = $27`. Do not equate ticks with dollars, even when their numerical values happen to match.

**Decision:** The new attempts demonstrate the corrected tick-value and movement calculations. Proceed to Part B, questions 9–13, while cleaning up the units in question 5. Part A written cleanup remains pending; this does not validate the entire week or assign a weekly score.

## Parts A and B — Review, 2026-09-15

Question 5 now correctly separates ticks from dollars. The outstanding Part A correction is resolved; Part A is validated after remediation.

Part B answers in `ASSIGNMENT.md` were checked against the exercise's actual fills and $2 round-trip fees per contract:

| Question | Gross P&L | Total fees | Net P&L | Assessment |
|---:|---:|---:|---:|---|
| 9 — Long 1 MES | +$31.25 | $2 | +$29.25 | Correct |
| 10 — Short 1 MES | −$17.50 | $2 | −$19.50 | Correct |
| 11 — Short 2 MNQ | +$30.00 | $4 | +$26.00 | Correct |
| 12 — Long 1 MGC | −$14.00 | $2 | −$16.00 | Correct |
| 13 — Short 1 MCL | +$17.00 | $2 | +$15.00 | Correct |

**Part B result: 5/5 correct.** Direction, multipliers, quantity, fee scaling, and net-result signs are correct; no additional slippage was double-counted. Minor notation refinement: in questions 12–13, label contract units as 10 ounces and 100 barrels rather than `$10` and `$100`; the dollar-per-ounce/barrel price difference supplies the currency unit. This does not change the correct results.

**Next:** Part C, questions 14–20. For 14–19, use a positive stop distance and add round-trip fees plus the total two-tick slippage allowance per contract. For 20, use actual fills and actual fees, then divide net P&L by initial planned risk for the result in R. No overall weekly pass or score is assigned yet.
