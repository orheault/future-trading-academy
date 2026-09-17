# Week 2 — Coach Review

## Part A — First submission, reviewed 2026-09-15

**Evidence:** Answers to questions 1–8 in `ASSIGNMENT.md`.
**Current status:** Parts A and B validated; Part C calculation rechecks passed 2026-09-16. Proceed to Part D; minor written cleanup remains in Q15/Q19. Earlier entries preserve the correction history.
**Assessment scope:** Parts A–C, as detailed below. No overall weekly score or pass assigned.

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

## Part C — First review, 2026-09-16

**Evidence:** Student answers to questions 14–20 in `ASSIGNMENT.md`, read on this date. Original answers left unchanged by the coach.
**Status:** Not yet validated. No overall weekly score assigned.

For 14–19, round-trip fees are $2 per contract and slippage allowance is two ticks TOTAL per contract. Price risk alone is not total planned risk.

| Question | Stop ticks | Price risk | Fees | Slippage allowance | Total planned risk | Budget decision for one contract |
|---:|---:|---:|---:|---:|---:|---|
| 14 — MES | 16 | $20.00 | $2 | $2.50 | $24.50 | Fits $25 |
| 15 — MES | 17 | $21.25 | $2 | $2.50 | $25.75 | Skip |
| 16 — MNQ | 40 | $20.00 | $2 | $1.00 | $23.00 | Fits $25 |
| 17 — MGC | 20 | $20.00 | $2 | $2.00 | $24.00 | Fits $25 |
| 18 — MCL | 22 | $22.00 | $2 | $2.00 | $26.00 | Skip |
| 19 — MES | 8 | $10.00 | $2 | $2.50 | $14.50 | Fits $25 |

### Question-specific feedback

- **14:** Fully correct.
- **15:** Correct dollar risk and budget conclusion. The stop-tick line is inconsistent: `6,000 − 5,995.75 = 4.25 points`, then `4.25 / 0.25 = 17 ticks`. Explicitly state: skip the trade; keep the scenario's necessary stop unchanged.
- **16–17:** Tick distances and price risks are correct. Fees and slippage were omitted from the reported total. The two-tick allowance has a different dollar value for MNQ than MES.
- **18:** Correct ticks and price risk, but omitted costs reverse the budget decision: $26 exceeds $25. This is a critical planned-risk error in a paper exercise, not evidence of an actual executed trade or safety incident.
- **19:** The $10 figure is price risk only. All-in risk per contract is $14.50. Risk-based quantity is `floor($25 / $14.50 per contract) = 1 contract`; academy cap is one Micro, so permitted quantity under these two checks is one. Dividing budget by tick value gives ticks, not a contract quantity. The student correctly withheld authorization, but including costs alone still would not authorize a trade: an eligible setup, valid context/invalidation, account/mode, and all other program checks are also required. No active execution setup is inferred here.
- **20:** Entry was copied as 6,000 rather than the actual 6,000.25. Gross P&L = `(5,995.75 − 6,000.25) × $5 = −$22.50`. Net = `−$22.50 − $2 = −$24.50`. Result = `−$24.50 / $24.50 = −1R`. The no-double-counting principle is correct; actual fills at BOTH entry and exit already reflect execution differences.

### Correction method and recheck

Before calculating, copy the exact prices and distinguish planning references from actual fills. For planning problems, use separate columns for stop ticks, tick value, price risk, fees, total slippage allowance, all-in risk, and decision. For sizing, divide dollars of budget by dollars of risk per contract, then round down to a whole contract and apply the academy cap.

Add revisions to questions 15–20 with units. Before moving to Part D, complete fresh checks:

1. One MCL has a 23-tick stop, $2 round-trip fees, and two ticks of total slippage allowance. Calculate price risk, all-in risk per contract, risk-based contract quantity for a $25 budget, and the decision.
2. One MES long actually fills at 6,000.50 and exits at 5,996.00; fees are $2 and initial planned risk is $24.50. Calculate gross P&L, net P&L, and R without adding slippage again.

Review revised critical calculations and new answers before validating Part C. The rest of Week 2 remains incomplete.

## Part C — Revised submission review, 2026-09-16

Read the revised student answers in `ASSIGNMENT.md`; no student answers were changed by the coach.

- **14:** Remains correct.
- **15:** Price risk $21.25, total $25.75, and budget rejection are correct. The first line still incorrectly equates `(6000 − 5995.75) × 4` with `4.25 points`. Separate `4.25 points` from `17 ticks`. State explicitly that the trade is skipped without moving the necessary stop.
- **16:** Corrected total $23, including fees and the $1 MNQ slippage allowance.
- **17:** Corrected total $24, including fees and slippage.
- **18:** Corrected total $26 and rejection of the trade.
- **19:** Corrected all-in risk $14.50 and final quantity one Micro. The intermediate 1.72 is a theoretical contract quantity, not dollars; write `floor($25 / ($14.50 per contract)) = 1 contract`. The academy's one-Micro cap is a separate restriction from its $25 budget. The old explanation claiming costs are excluded is now false: costs ARE included in the revised calculation. Risk compliance alone does not establish setup eligibility or satisfaction of the other program checks.
- **20:** Corrected gross −$22.50, net −$24.50, and −1R. Refine the explanation to mention actual entry AND exit fills, not exit alone.

**Decision:** Substantial arithmetic corrections accepted; Part C not yet validated. Resolve Q15/Q19 wording and units, and submit the two fresh checks above. No answers to those checks were found in the reviewed assignment or review file.

## Part C — Independent checks submitted in conversation, 2026-09-16

1. **MCL risk/sizing: passed.** Student calculated $27 all-in risk and rejected the trade because $25/$27 is below one contract. Make the whole-contract result explicit: floor(25/27) = 0 contracts. The quoted 0.92 is a truncated approximation (approximately 0.93 rounded); this does not change the correct decision.
2. **MES actual-fill P&L/R: not yet passed.** Student used entry minus exit for a long, reporting +$22.50 gross, +$20.50 net, and +0.83R. A long sold below its entry loses money. Correct calculation: (5,996.00 − 6,000.50) × $5 = −$22.50 gross; −$22.50 − $2 = −$24.50 net; −$24.50/$24.50 = −1R. This is a direction/sign error, not a new slippage charge.

**Next check:** For one MES long entered at 6,000.75 and exited at 5,997.25, with $2 round-trip fees and $25 initial planned risk, identify gain/loss before computing gross P&L, net P&L, and R. Part C remains pending this correction and the previously requested written cleanup; no later file edits were inferred from this chat response.

## Part C — Final calculation recheck, 2026-09-16

Student correctly identified a loss before calculating: `(5,997.25 − 6,000.75) × $5 = −$17.50` gross; `−$17.50 − $2 = −$19.50` net; `−$19.50 / $25 = −0.78R`. Together with the passed MCL check, this satisfies the requested independent calculation rechecks after remediation.

The assignment was reread. Q15 now explicitly gives 17 ticks, though the preceding expression still contains a stray `× 4` before `= 4.25 points`; remove that factor in the point-distance expression. Q19 now gives contract units and rounds down correctly. Refine “scenario not admissible” to “risk compliance alone does not establish scenario eligibility or completion of the other checks”; the calculation alone does not establish that a hypothetical setup fails. Q20 now correctly refers to both actual entry and exit fills.

**Decision:** Part C calculations validated after remediation; proceed to Part D, questions 21–25. Finish the small Q15/Q19 written refinements alongside that work. Original student wording is left untouched. This is not completion of Week 2 or authorization to trade.
