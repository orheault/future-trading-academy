# Week 2 — Coach Review

## Part A — First submission, reviewed 2026-09-15

**Evidence:** Answers to questions 1–8 in `ASSIGNMENT.md`.
**Current status (2026-09-24):** Week 2 passed after remediation, **85/100**. Final rubric and evidence assessment appear at the end of this document. Prior pending decisions below are retained as dated history.
**Assessment scope:** Written work and fresh rechecks, platform preparation screenshots, coached quiz responses, student notes, reflection and Study Log. This is a rubric-based instructor assessment after remediation, not an unassisted exam percentage or proof of independent live execution readiness.

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

## Part D — Question 21 review, 2026-09-17

Student calculated spread as `6000.25 − 6000 = 0.25 $`, gross P&L −$1.25, and net P&L −$3.25.

**Assessment:** Gross and net P&L are correct. The spread is **0.25 index points**, not $0.25; explicitly convert to **1 tick** using 0.25 points / (0.25 points per tick). The equivalent dollar spread for one MES is $1.25. Buying at the ask and selling at the bid in this fixed-quote example creates a gross loss even without a change in quotes. Actual fills already include that spread; subtract only the $2 round-trip fee from gross P&L here.

**Next:** Clarify the spread line and proceed to Q22 (8-tick target and estimated costs). Restored the shifted question labels 23–26 to their original 22–25 in the assignment; student answers were preserved. Other Part D answers were not present.

## Part D — Question 22 review, 2026-09-17

Q21's revised spread line correctly states 0.25 points = 1 tick; Q21 is validated.

For Q22, the student's $10 gross target and $5.50 estimated net profit are correct. The reported `5.5/10 = 0.55 %` has two issues:

- $5.50 is the remaining net profit, not the costs. Estimated costs = $2 fees + 2 ticks × $1.25/tick = $4.50.
- A decimal ratio must be multiplied by 100 to express a percentage: costs / gross = 4.50/10 = 0.45 = **45%**. The net share is 5.50/10 = 0.55 = **55%**, not 0.55%.

**Next:** Revise the cost-percentage line without erasing the original attempt. Short comprehension check: with $20 gross profit and $5 total costs, calculate costs as a percentage of gross and the percentage remaining net. Q22 percentage correction/check remains pending; no answer to Q23–25 was present in the reviewed section.

## Part D — Question 23 review, 2026-09-17

Student answers were read in `ASSIGNMENT.md` and left unchanged. Q23 slippage is correct: (5,996.00 − 5,995.25) / 0.25 = 3 ticks, equivalent to $3.75 for one MES.

The actual loss before fees is correctly calculated as $23.75. The reported final $25.75 loss is correct, but `23.75 − 2 = 25.75` is an invalid equality. With losses expressed as positive amounts, write **23.75 + 2 = $25.75**. Alternatively, signed net P&L is **−23.75 − 2 = −$25.75**.

The excess-loss result is incorrect. The reference here assumes an exact stop fill plus the same fees, not a slippage allowance:

- Planned reference loss: (6,000 − 5,996) × $5 + $2 = **$22**.
- Actual net loss: (6,000 − 5,995.25) × $5 + $2 = **$25.75**.
- Excess loss, positive amount: $25.75 − $22 = **$3.75**.

The $2 fees occur in both scenarios and cancel when comparing their losses. Do not subtract or add them again to the three-tick execution difference. Signed actual-minus-reference P&L is −$3.75; it describes the same deterioration with a different sign convention. The student's `3 × 1.25 − 2 = −5.75` is invalid; the expression itself equals +$1.75 and is not the required comparison.

Q22 now uses the correct numerator ($4.50 costs), but still writes `4.5/10 = 0.45 %`. Correct notation: **4.5/10 = 0.45 = 45%**. The earlier fresh percentage check remains unanswered in the conversation.

**Next:** Correct Q23's fee sign and excess-loss comparison, and Q22's percentage notation. Q23 is not yet validated. Restored the last two question labels from 25/26 to 24/25 without changing their content or student answers.

## Part D — Question 24 review, 2026-09-17

Student correctly answered that the exit is not assured and correctly calculated unrealized gross P&L: `(5,994 − 6,000) × $5 = −$30`, equivalently −24 ticks × $1.25. The position remains open in the stated no-fill scenario, so this is unrealized gross P&L at the specified mark, not a realized exit or a loss cap.

The explanation “the max is 5995.75” reverses the price constraint. For a **sell limit**, 5,995.75 is the **minimum acceptable sale price**. The trigger at 5,996 activates the limit order; a bid of 5,994 is below the minimum and cannot fill that sell order. A buy limit instead defines a maximum acceptable purchase price. Revise this explanation before marking Q24 fully validated. Reference: [CME futures order types](https://www.cmegroup.com/education/courses/futures-trading-mechanics-and-regulation/futures-order-types).

Other visible revisions: Q22 now correctly states 0.45 = 45%; its written answer is corrected (the separate percentage practice question has not been answered). Q23 now correctly writes net P&L −$25.75, but its excess-loss line is unchanged and incorrect; replace with $25.75 − $22 = **$3.75 additional loss**, with no additional fee subtraction. Original student answers were left intact.

**Next:** Correct Q24's minimum/maximum distinction and Q23's remaining excess-loss line; then complete Q25. No new exercise is required at this point and no overall weekly pass is assigned.

## Part D — Question 25 review, 2026-09-17

The assignment now correctly gives Q23 excess loss as $3.75 and describes Q24's sell limit as a minimum sale price. Those written corrections are accepted.

For Q25:

- **Target offset:** correct, 6 points / 0.25 = 24 ticks above entry.
- **Stop offset:** direction is below entry, but the written chain mixes signs: `5,996 − 6,000 = −4 points`, then `−4 / 0.25 = −16 ticks`. Alternatively express a positive distance of `abs(5,996 − 6,000) / 0.25 = 16 ticks below entry`. A signed relative displacement is valid if stated consistently; this is not an instruction to enter a negative distance in a platform field.
- **Net profit:** correct, 24 × $1.25 − $2 = $28, given exact entry/target fills in the exercise.
- **OCO explanation:** incomplete. A bracket describes the entry with attached stop/target; OCO links the sibling exits. Once the target completely fills the one-contract long exit, the linked protective sell stop is intended to be canceled. Verify actual target fill and quantity, position quantity zero (flat), confirmed stop cancellation, and no unintended working orders for this trade. Reviewing execution prices/P&L is useful but does not replace those checks. A leftover executable sell stop could open an unintended short if it later fills, depending on service/order safeguards.

Reference: [Sierra Chart Attached Orders](https://www.sierrachart.com/index.php?page=doc/AttachedOrders.html). Actual order-management implementation depends on the selected service; the exercise asks for the intended behavior and verification, not a claim of infallible cancellation.

**Next:** Correct Q25's stop notation and explain cancellation/flat-position checks in the student's own words. Part D remains pending that explanation; the platform lab, closed-book quiz, and weekly evidence remain separate requirements. Student answers were preserved.

## Part D — Question 25 reformulation, 2026-09-17

The revised explanation recognizes intended cancellation when the objective is executed and the risk of an unintended short from a remaining sell stop. This is accepted progress. Make the scope precise: the linked OCO stop is intended to be canceled after full target execution; unrelated orders are not necessarily canceled. The answer still mentions checking slippage but omits the requested operational confirmations: actual full target fill, zero remaining position, and confirmed cancellation of the linked stop/no unintended working order for the trade. These confirmations are needed rather than assuming the intended OCO action occurred.

The stop is now described correctly as 16 ticks below entry, but `5996 − 6000 = 4 points` is still a false equality. Use `(6000 − 5996) / 0.25 = 16 ticks below entry` for the positive distance. Target offset and $28 net profit remain correct.

Q15's point/tick expression and Q19's strategy/risk explanation were reread and are now corrected. Combined with the prior passed calculation rechecks, Part C is validated after remediation. No outstanding Q15/Q19 cleanup remains.

**Next:** Finish the Q25 equation and add explicit confirmation of fill, flat position, and stop cancellation. No additional numerical exercise assigned. Part D and the full week are not yet marked complete. Student answers left unchanged.

## Part D — Question 25 final review, 2026-09-17

The student added all three required checks: full target fill for one contract, zero remaining position, and confirmed cancellation of the linked OCO stop with no residual order for the trade. These are correct statements of the checks to perform in the hypothetical exercise, not evidence of a real platform execution. The explicit linked-stop wording resolves the earlier ambiguity about which orders are canceled.

The distance is correctly described as 16 ticks below entry, but the written numerator remained `5996 − 6000` while the result was positive. The coach corrected the numerator to `6000 − 5996` and added an attributed note preserving the original expression and explaining its signed result. This editorial correction is not represented as an independent student calculation.

**Decision:** Written Parts A–D are reviewed and accepted after corrections/remediation. No further rewrite cycle is required for Q25. Overall Week 2 remains in progress: the closed-book concept quiz will assess independent understanding; the contract/platform lab, student notes, study log, and weekly review require completion/verification. No weekly score, platform completion, or trade authorization is inferred.

## Platform lab — Question 1 screenshot evidence, reviewed 2026-09-18

Source: `journal/screenshots/week-01/Capture d’écran 2026-09-03 212213.png`, visually inspected. The Windows taskbar shows 2026-09-03; the chart/application timestamps show 2026-09-04. No timezone setting is visible, so the difference is not treated as an error or used to infer the configured timezone.

Visible at capture time:

- Sierra Chart installed/running, version 2947.
- Chartbook `FTA-01-SAFETY-SIM`.
- `[Sim]` in the application title and account `Sim1` in the trade window: evidence of simulation at capture time.
- `Delayed` in the chart title: delayed data for the displayed MES chart.
- `SC Data` label in the application title. The exact `Current Selected Service` setting is not displayed; do not equate this abbreviated label with a verified full service setting.
- Symbol `MESU26-CME[M]`, September 2026 MES, one-minute chart.
- Position display `Flat`. This does not prove there were no working orders elsewhere.

Updated the previously stale installed-status field in `PROGRESS.md`. This historical screenshot supports question 1 but does not establish present-day settings, current active expiry, bracket configuration, or completion of either week's entire platform lab. Next: confirm the exact Current Selected Service value and whether the observed simulation/delayed-data settings remain current. No platform actions or orders were performed.

### Question 1 — Student service confirmation, 2026-09-18

Student reports `SC Data` selected in the service settings. Recorded this as current student-reported service evidence in the assignment and progress log. Current `[Sim]`/`Sim1` and delayed-data status have not yet been reconfirmed; the prior screenshot remains historical evidence for those fields. No change to platform settings was requested or performed.

### Question 1 — Complete, 2026-09-18

In subsequent messages, the student explicitly confirmed `[Sim]`, `Delayed`, and finally `Sim1` in the Trade Window. Together with the confirmed `SC Data` setting and installation evidence, this completes the setup inventory requested by platform question 1. Current settings are student-reported, not a fresh screenshot inspection. No trade or settings change was performed by the coach.

Next: question 2, beginning with the exact current MES chart symbol and observation/replay date. The September symbol in the old screenshot does not establish the current symbol or active expiry. Volume comparison and dated contract selection evidence remain pending. Overall platform lab and Week 2 remain incomplete.

### Question 2 — Symbol recorded, 2026-09-18

Student reports `MESZ26-CME`. Parsed as MES, December (Z), 2026; retained the displayed CME suffix exactly. Record date is the conversation date, not an inferred chart/replay timestamp. Need to establish whether this is current delayed observation or historical replay, then document relevant expiry volumes for that session before validating the active-contract choice. No expiry date, volume, or rollover event was inferred from the symbol alone.

### Question 2 — Observation mode confirmed, 2026-09-18

Student confirms the chart follows the current delayed market rather than historical replay. Next evidence needed: observation time/session and comparable total session volumes for the relevant MES expiries, including December 2026. Do not substitute individual candle volume for contract session volume or presume the active expiry from the displayed symbol alone.

### Question 2 — Daily Volume reports zero, 2026-09-18

Student reports Daily Volume = 0. Treat this as an unverified quote-field reading, not established zero trading activity or evidence that December is inactive. No diagnosis is confirmed. Request the Current Quote Window's displayed symbol, date/time, and Last/Bid/Ask values (or a screenshot) to check quote identity and freshness before changing configuration or using this value in an expiry comparison. No settings changed; question 2 remains pending.

### Question 2 — Quote timestamp and prices supplied, 2026-09-18

Student reports timestamp `2026-09-18 20:59:59.707 Fri`, timezone UTC+0, Last 7,725.50, Bid 7,725.25, Ask 7,725.50. That timestamp converts to 16:59:59.707 Toronto (EDT), consistent with just before the normal Friday close. The supplied spread is 0.25 points, one MES tick. These populated price fields do not establish a functioning current connection or explain Daily Volume = 0; zero is not accepted as comparative liquidity evidence.

Fallback for the learning exercise: compare contract-specific Historical Daily volumes for the same completed session (proposed 2026-09-17), recording that this is prior-session evidence rather than the live volume on 2026-09-18. Before using those values, verify `Download Total Volume for All Contracts for Futures Daily Data` is No, and use specific-expiry, non-continuous charts. Sierra's documentation says Yes aggregates all expiries and No gives the individual contract volume. No setting change or alternative volume observation is yet confirmed.

### Question 2 — Historical volume setting confirmed, 2026-09-18

Student confirms `Download Total Volume for All Contracts for Futures Daily Data` is **No**. No change required. Next: open separate Historical Daily charts for MES September 2026 and December 2026, verify no continuous-contract stitching, and read the Volume of the 2026-09-17 daily bar on both charts. The comparison date precedes the current Friday session and must be labeled accordingly. Actual volumes remain pending; if existing files were downloaded under different settings their provenance would need checking before relying on them.

### Question 2 — December daily volume captured, 2026-09-18

First submitted daily-chart screenshot displayed `Tue 2026-03-17` in Chart Values for Tools, with Volume 2. That was a March bar, not the requested September session; this explains that particular reading, not the separate Current Quote Window Daily Volume zero.

The next screenshot visibly shows `MESZ26-CME[M]`, `Daily`, and `Thu 2026-09-17` selected. Recorded **Volume 1,014,522 contracts** for the displayed December chart on that session. Open interest is separately displayed as 108,133 and was not mistaken for volume. Evidence saved to `journal/screenshots/week-02/2026-09-17_MESZ26_daily-volume.png` from the user-supplied image.

Next: obtain the corresponding daily Volume for `MESU26-CME` on **2026-09-17**, using the same data basis. The No setting for all-expiry volume aggregation was confirmed earlier; Continuous Contract = None has been requested but not explicitly confirmed. Contract-specific comparison and active-contract conclusion remain pending. No live-session volume or present-day trade eligibility is inferred from this historical reading.

### Question 2 — September volume and comparison recorded, 2026-09-18

The user-supplied screenshot visibly shows `MESU26-CME[M]`, Daily, selected bar `Thu 2026-09-17`, **Volume 123,498**, and separate OpenInt 260,677. Saved the evidence to `journal/screenshots/week-02/2026-09-17_MESU26_daily-volume.png`. The earlier September-chart screenshot had the cursor on 2026-09-24 and its zero was not used.

Same selected session comparison: December 1,014,522 / September 123,498 = approximately **8.21**. December accounts for about 89.15% of the combined volume of these two expiries only. This supports choosing December as the more actively traded of the two based on 2026-09-17 data; it does not prove every aspect of liquidity or a guaranteed fill. The two screenshots and prior-session basis are recorded in the assignment.

Remaining verification for question 2: student confirmation that Continuous Contract = None on both charts; its setting is not visible in these images. Do not mark that configuration check complete by inference. After confirmation, continue to question 3 (specifications and expiry). Closed-book quiz and other weekly evidence remain outstanding.

### Question 2 — Final configuration confirmation, 2026-09-18

In response to the check for both charts, the student confirms “OUi bien sur none”. Continuous Contract = None is therefore recorded as student-confirmed, not screenshot-verified. Together with the previously confirmed No aggregation setting and the two same-session screenshots, this completes question 2 for the exercise. December is supported as the more actively traded of the two compared expiries on 2026-09-17. Continue with question 3: official contract specifications, expiry, financial settlement, and the distinction between changing a chart symbol and rolling an open position. Week 2 remains in progress.

### Question 4 — Bracket preparation screenshots reviewed, 2026-09-22

Saved both student screenshots under `journal/screenshots/week-02/`: `2026-09-22_bracket-main.png` and `2026-09-22_bracket-targets-stop-limit.png`. Simulation indicator, Sim1, Flat, parent limit 6,000, quantity 1, and Use Attached Orders enabled are visible. Target 1 is Limit, 24 ticks, quantity 1; Stop 1 is Stop Limit, 16 ticks, quantity 1, OCO Group 1. The target's group selector is not shown. The $30 target and $20 stop amounts are gross price distances, not net results or a guaranteed maximum loss.

Offsets are accepted. The original prompt did not specify a stop subtype; this is a coaching clarification, not a previously stated requirement the student failed. For this simulation preparation, request `Stop: Stop` and explain that a triggered Stop Limit may remain unfilled if its limit prevents execution. Keep 16 ticks, quantity 1, OCO Group 1, and confirm the target uses the same group. Updated screenshot requested without submitting any order. Flat is current position evidence only, not proof of no working orders or prior submissions. Question 4 remains pending final configuration review; question 3 and the quiz remain outstanding.

References checked: Sierra Chart Attached Orders and Order Types documentation.

### Question 4 — Corrected stop verified, 2026-09-22

Saved the new screenshot as `journal/screenshots/week-02/2026-09-22_bracket-targets-stop.png`. Visible selected Stop 1: Type `Stop: Stop`, Offset Type Ticks, Stop Offset 16, Quantity 1, OCO Group 1. Stop configuration accepted. Target 1 remains listed as Limit / 24 ticks / quantity 1; its group selector is still not displayed. Request selection of Target 1 and confirmation of OCO Group 1 to finish the configuration review. No order submission requested or inferred.

### Question 4 — Target group verified; preparation complete, 2026-09-22

Saved `journal/screenshots/week-02/2026-09-22_bracket-target-selected.png`. Selected Target 1 visibly shows `Target: Limit`, Offset Type Ticks, Limit Offset 24, Quantity 1, OCO Group 1. Combined with prior Main-tab and corrected Stop 1 screenshots, the preparation requirement for question 4 is complete. Both attached orders use the same OCO group. This is configuration evidence only, not an execution or cancellation test, and no submission is requested or inferred. Next: obtain the student's question 3 specification/settlement/roll explanation. Closed-book quiz and remaining weekly evidence are still outstanding; Week 2 remains in progress.

### Question 3 — Specifications accepted; explanation pending, 2026-09-22

Reviewed the student's four added lines in ASSIGNMENT.md. Correct: outright tick 0.25 points = USD 1.25 per contract; multiplier USD 5 times the index; December 18, 2026 last trade date for MESZ26 under the third-Friday rule; financially settled. Official reference rechecked: https://www.cmegroup.com/rulebook/CME/IV/350/353/353.pdf (35301, 35302.C/G, 35303). The required distinction between changing a chart symbol and rolling an open position is absent. Request a short explanation in the student's own words before completing question 3 and advancing to the closed-book quiz. No student answer was replaced or supplied as student evidence.

### Question 3 — Rollover explanation accepted, 2026-09-22

Student explains in chat that rollover closes September and opens December; original wording preserved in ASSIGNMENT.md. Accepted after coaching, with instructor clarification that merely switching the chart leaves the original position unchanged. Question 3 and platform preparation lab questions 1–4 are complete. This is completion after feedback, not a closed-book mastery score or live trading authorization. Begin the existing closed-book quiz with question 1 (tick, point, tick value, multiplier). Week 2 remains in progress pending quiz and other weekly evidence.

### Closed-book quiz — Question 1 reviewed, 2026-09-22

Original chat answer preserved in ASSIGNMENT.md. Correct minimum-increment definition, relationship between tick size and ticks per point, multiplier as dollar value per point, and MES USD 5/point and USD 1.25/tick. Accepted with instructor clarification: one point is one quoted-price unit; MES tick size 0.25 point gives four ticks per point. The explicit 0.25/four-tick values were not supplied by the student in this response. No overall score assigned. Continue to question 2: distinguish notional exposure, margin, and planned risk-to-stop.

### Closed-book quiz — Question 2 needs remediation, 2026-09-22

Student answer preserved verbatim in ASSIGNMENT.md. Broadly correct notional/margin definitions and explicit recognition that margin is not maximum loss. Two issues remain: planned dollar risk needs tick-value conversion before adding fees, and the final assertion incorrectly ties maximum loss to account balance relative to notional exposure. Clarify leverage versus loss and that futures losses can exceed deposits (NFA Investor Best Practices, checked 2026-09-22). Use a new hypothetical USD 500 starting balance / USD 650 realized net loss to check understanding before moving on. Question 2 remains pending; no overall score or risk mastery pass assigned.

### Closed-book quiz — Question 2 remediation accepted, 2026-09-22

Student correctly calculates a USD −150 balance and explicitly states that USD 500 did not limit the loss. Original wording preserved in ASSIGNMENT.md. Clarify that the loss exhausts USD 500 and exceeds it by USD 150. Loss-cap remediation accepted; question 2 accepted after feedback, with monetary-risk unit conversion recorded as instructor clarification rather than independent student evidence. Continue to question 3 on why planned stop risk is not a maximum possible loss. No overall score or weekly completion assigned.

### Closed-book quiz — Question 3 accepted, 2026-09-23

Student independently identifies slippage exceeding its planned allowance and market execution speed as reasons for excess loss. Original answer preserved in ASSIGNMENT.md. Core answer accepted. Coach clarifies that rapid price movement and/or execution delay can produce a worse fill, and a stop trigger level is not a guaranteed fill price; faster execution itself is not inherently a cause of loss. Continue to question 4 on double-counting slippage when actual fills are used. No total quiz score or weekly completion assigned.

### Closed-book quiz — Question 4 accepted, 2026-09-23

Student correctly states that no additional slippage allowance should be deducted because slippage is already included in the exit fill. Original wording preserved in ASSIGNMENT.md. Accepted with a scope clarification: actual entry fills also incorporate entry slippage. Actual commissions/fees remain deductible from gross fill-based P&L. Continue to question 5: offset, rollover, final settlement, and why the third-Friday expiry rule is not universal. No overall score or weekly completion assigned.

### Closed-book quiz — Question 5 remediation required, 2026-09-23

Original answer preserved in ASSIGNMENT.md. Student correctly describes rollover closing one expiry and opening another but incorrectly presents offset and final settlement as successive steps intended to receive the underlying. Clarify equal/opposite same-expiry offset ends the position; positions held to expiry undergo contract-specific settlement, which is cash for MES. Distinguish expiry settlement from realized P&L and daily variation settlement. Third-Friday universality question was unanswered. Official CME expiration/roll lesson and MES Chapter 353 rechecked. Follow-up checks a December MES round trip before expiry, MES cash versus share delivery at expiry, and whether gold/crude expiry can be inferred from MES. Q5 remains pending; no overall score assigned.

### Closed-book quiz — Question 5 remediation accepted, 2026-09-23

All three follow-up answers are correct and preserved in ASSIGNMENT.md. Student recognizes that full offset leaves no position to settle at expiry, MES held to expiry is financially settled, and expiry details must be obtained from the exchange's contract information page (CME in this exercise). Accept question 5 after remediation, preserving the initial misconception and its correction. Continue to question 6: potential stop-limit non-execution and bracket/OCO failure plus checks after a target fill. Quiz questions 6–8 and other weekly evidence remain outstanding; no total score or week completion assigned.

### Closed-book quiz — Question 6 remediation needed, 2026-09-23

Student honestly reports uncertainty about stop-limit non-execution; correctly identifies unintended short risk from an orphan sell stop after closing a long; mentions checking both orders and fill/slippage review. Original answers preserved in ASSIGNMENT.md. Need explicit distinction between target Filled and stop Canceled, position Flat/zero, and absence of residual associated orders. Explain triggered sell stop-limit cannot execute below its limit and may leave the long exposed. Sierra Chart Order Types documentation rechecked. A new numeric example and a status-check question will test understanding; Q6 not yet validated. No score or week completion assigned.

### Closed-book quiz — Question 6 remediation accepted with clarification, 2026-09-23

Original follow-up answers preserved in ASSIGNMENT.md. Student correctly reasons that a sell limit at 6099.50 cannot execute against the prompt's best bid 6099.00 and the position stays open. Their written 9099.00 is treated explicitly as a likely typo, not silently corrected or accepted literally. They identify full closure and no remaining associated orders. Accept Q6 after remediation, clarifying that the precise stop status is Canceled, while the target is Filled and the position Flat/zero. Exact English status terminology was supplied by the coach, not independently reproduced by the student. Continue with historical-replay expiry selection (Q7); no overall score or weekly completion assigned.

### Closed-book quiz — Question 7 partially complete, 2026-09-23

Student identifies File/Find Symbol and comparison of volume with the next expiry. Original answer preserved in ASSIGNMENT.md. Volume-comparison principle accepted, historical date/time basis missing. Ask the student to distinguish current volumes from volumes relevant to a 2026-09-17 replay. When coaching a decision made before session open, distinguish preceding completed-session evidence from full replay-day volume only known afterward. No assumption that the student has already addressed this temporal issue. Q7 remains pending; Q8 and remaining weekly evidence are outstanding.

### Closed-book quiz — Question 7 accepted after prompting, 2026-09-23

Student responds that the historical replay period must be checked; exact wording preserved in ASSIGNMENT.md. Combined with the initial expiry-volume comparison, accept Q7 after prompting. Coach adds equal historical time basis and use of information available at the selection time (e.g. previous completed session when choosing before open). No independent student mastery of that finer timing distinction is inferred. Continue to Q8 on zero permitted contract quantity; no total score or weekly completion assigned.

### Closed-book quiz — Question 8 no-trade decision accepted, 2026-09-23

Student correctly declines the trade because USD 28 planned risk per contract exceeds the USD 25 budget. Original chat answer preserved in ASSIGNMENT.md. The original Q8 zero-quantity decision is correct; the additional stop-adjustment question in the chat prompt remains unanswered. Request the student's explanation of whether a stop may be moved solely to fit the budget before closing the quiz review. No total score or weekly completion assigned; remaining weekly deliverables still need review.

### Closed-book quiz — Question 8 accepted; quiz review complete, 2026-09-23

Student correctly explains that moving the stop solely to meet budget would violate the strategy and risk an earlier exit from ordinary price movement. Exact follow-up preserved in ASSIGNMENT.md. Q8 accepted; all eight quiz items reviewed and accepted with remediation history preserved. This is not a claim of independently correct first-attempt answers. Section 7 of notes/contract-math.md was checked and remains blank. Study Log has not been inspected in this turn; no attendance is inferred. Next: student personal notes and new long/short examples, Study Log review, four-part weekly reflection, then final assessment against the curriculum. No weekly pass or numerical score assigned.

### Student notes — Section 7 first review, 2026-09-23

Read all five newly completed entries in notes/contract-math.md; preserve the student's wording unchanged.

1. Tick/point: broadly correct. Clarify one point is a 1.00 change in quoted price, rather than an arbitrary chart graduation; for MES, 0.25 point/tick and four ticks/point. Multiple ticks per point is product-specific, not a universal rule.
2. Notional/margin/planned risk: broadly correct. Margin is collateral to open and maintain the position. Planned risk is specifically the estimated loss to the initial stop plus fees and estimated adverse execution, not a guaranteed maximum.
3. Examples: long entry 6000, target 6005; short entry 6000, target 5990. Direction is correct; quantity, execution assumptions and P&L calculations absent. Request completion using one MES, assumed actual entry/exit fills exactly at those prices, and USD 2 total round-trip fees. Instructor check: long +5 points / +20 ticks / USD 25 gross / USD 23 net; short favorable 10 points / 40 ticks / USD 50 gross / USD 48 net. These are hypothetical fills supplied for the follow-up, not evidence of an actual trade or guaranteed target execution.
4. Student writes: “It depends if this is the p&l brut or net. p&l net does not include slippage because it is include in the exit price. The brut must include the estimated slippage. both cases must include round trip cost.” This is incorrect despite the earlier accepted quiz response: distinguish reference prices from actual fills separately from gross/net. Gross actual P&L uses actual entry/exit fills without deducting fees or a slippage allowance; net subtracts actual fees. Actual fills already incorporate execution effects on both sides. Forecast net P&L based on reference prices subtracts estimated costs/execution allowance. Cost-accounting understanding requires renewed application before weekly validation.
5. Student describes an unwanted short from a remaining OCO order and proposes checking remaining orders are flat. Scenario mechanism is correct; exact statuses need correction: position Flat/zero, target fully Filled, linked stop Canceled, no residual associated orders. The student's past-tense example alone does not establish that a real or simulated incident occurred; no trade or safety failure is inferred without evidence. If intended as hypothetical, label it as such.

Next: student revises point 4 in their own words, completes both numeric examples under the stated assumptions, and sharpens point 5 status language. Study Log not inspected; no attendance or weekly pass inferred.

### Student notes — Section 7 revised submission, 2026-09-24

Read revised notes and preserve student text unchanged. Point 2 now includes maintaining a position and risk to the stop; accepted. Point 3 correctly computes the requested one-MES examples with USD 2 round-trip fees: long 5 points / 20 ticks / USD 25 gross / USD 23 net; short favorable 10 points / 40 ticks / USD 50 gross / USD 48 net. Accept under the coach's stated assumption of fills exactly at entry/target prices. Point 5 now explicitly checks position Flat, objective entirely executed, stop canceled and no residual orders; the example is explicitly hypothetical. Accepted, with no actual trade incident inferred.

Point 1 now says “A point represent 1$ of price value on the chart.” This incorrectly identifies an MES index point as one dollar. Clarify a 1.00 change in quoted index level (e.g. 6000 to 6001), with USD 5 P&L per MES contract, and note ticks per point varies by product. Point 4 now reproduces the coach's correct actual-fills versus reference-prices explanation. Correct notes text is accepted as reference material, but copying does not establish independent mastery after the recurrent confusion. Ask a new application: one MES long, actual entry 6100.25, actual exit 6104.75, USD 2 actual round-trip fees, original planned slippage allowance 2 ticks. Student must calculate net realized P&L and state treatment of that allowance. Instructor check: 4.50 points, USD 22.50 gross, USD 20.50 net, no extra allowance deduction. These answer values are coach-only until the student responds. No final weekly score or pass; Study Log still uninspected.

### Student notes — Independent cost application reviewed, 2026-09-24

Student response: “Net: ( 6104.75 - 6100.25) * 4 * 1.25 - 2 = 19.25$” and “Je ne prend pas en compte la provision de 2 ticks, car le slippage est compris dans le prix réellement exécuté.” Formula, units conversion and no-extra-slippage reasoning are correct; arithmetic result is incorrect. Coach correction: 4.50 points × 4 ticks/point = 18 ticks; × USD 1.25/tick = USD 22.50 gross; − USD 2 fees = USD 20.50 net. Record this as correct independent method with instructor-corrected arithmetic, not an entirely correct unassisted calculation. Recommend retaining the intermediate lines as an arithmetic check.

Re-read point 1: student now writes “A point represent an increment of 1 on the chart, equal of 5$.” The point-versus-dollar confusion is corrected for the MES example; clarify that USD 5/point is specific to one MES contract, not universal. Section 7 accepted after these corrections, preserving original attempts and instructor contributions. Study Log, four-part weekly reflection and final assessment remain outstanding. No attendance inferred and no weekly pass assigned.

### Weekly reflection and Study Log review, 2026-09-24

Student's four-part reflection preserved in ASSIGNMENT.md: strength in planned risk and respecting the plan; recurrent arithmetic/transcription errors; no current uncertainty reported; interest in developing a strategy. Reflection received. Coach recommends explicit intermediate units and a second-method arithmetic check as the immediate practice goal. Formal setup specification occurs in curriculum Week 13; Week 3 is fundamental context. Self-reported clarity does not erase earlier conceptual remediation.

Read journal/trading-journal.xlsx without changing or exporting it. Inspected Study Log rows 1–205; week-2 entries occupy rows 14–22. Headers A5:I5: Study ID, Date, Week, Topic, Completed, Key Learning, Open Question, Evidence Link, Duration (min). Missing Study IDs A14:A22; dates B14:B19; durations I15, I21, I22. Existing durations I14/I16/I17/I18/I19/I20 total 360 minutes, a partial recorded total only. Lab, Quiz and Part 7 entries exist (rows 20–22); recent dates and additional duration must not be inferred from chat timestamps. Some learning/evidence cells remain blank; links are generic text references. Request the missing actual session details, preserving unknowns or clearly labeled estimates rather than fabricating attendance. No workbook modifications made. Final scoring deferred until journal completeness can be assessed; no weekly pass assigned.

### Study Log — Updated identifiers and dates verified, 2026-09-24

Reopened the workbook read-only after the student's update. A14:A22 now contains unique IDs W02-1 through W02-9; B14:B22 has date values. The previously missing dates and identifiers are filled. Durations I15 (W02-2, risk questions), I21 (W02-8, Quiz), and I22 (W02-9, Part 7) are still blank. Existing recorded durations still total 360 minutes; this is not a complete weekly duration. No workbook edits or export performed. Request these three actual durations, or an explicit unknown/labeled estimate if exact duration cannot be recovered. No new missing-time requirement added; these are the same three omissions identified in the first review. Final assessment remains pending.

## Final Week 2 assessment — 2026-09-24

**Decision: Pass after remediation — 85/100.** Apply CURRICULUM.md's existing weights and 80/100 threshold. Scores below are instructor judgments based on the complete evidence and learning process, not counts of independently correct first attempts.

### Final Study Log check

Read journal/trading-journal.xlsx without modifying/exporting it. Study Log I15 now contains 30 minutes, I21 40 minutes, and I22 30 minutes. Nine week-2 records A14:I22 have IDs, dates, topics, completion statuses and durations. I14:I22 sums to **460 minutes (7 hours 40 minutes)**. This is student-reported recorded time, not independent attendance verification. W02-1 remains Partial, appropriately preserving an unfinished initial block later continued; not every study block must itself be marked complete. Key Learning/Evidence Link fields remain sparse on some rows; generic evidence references are traceable through this review. Journal is sufficient for assessment with the quality deduction below; do not invent additional hours to match the nominal eight-hour plan.

### Weighted rubric

| Component | Score | Evidence and rationale |
|---|---:|---|
| Concept comprehension | 19/25 | All eight quiz topics ultimately accepted. Distinctions involving account loss limits, offset/final settlement, stop-limit execution and historical volume required prompts/remediation; cost-accounting confusion recurred in notes before a correct independent method was demonstrated. |
| Practical lab | 30/35 | All 25 written exercises reviewed and corrected, with fresh tick-value/risk/P&L checks. Dated expiry-volume comparison and unsubmitted one-contract bracket verified. Deduct for initial sign/cost/percentage errors and the later USD 19.25 versus USD 20.50 arithmetic result corrected by the coach. |
| Deliverable quality | 18/20 | Contract-math reference and student explanations, worked long/short examples, platform screenshots and weekly reflection are present. Unit/status wording needed correction; some reference wording was reproduced rather than independently formulated. |
| Journal completeness | 8/10 | Nine session records now include required identifiers, dates and durations; 460 minutes recorded. Learning details and evidence references could be more precise. |
| Process and risk compliance | 10/10 | Student demonstrates skip when one contract exceeds budget, refuses to move the stop solely to fit budget, and corrects OCO/position checks. Simulation/account evidence is present. No critical operational safety failure is evidenced in the reviewed work; screenshots alone are not proof of every historical order action. |
| **Total** | **85/100** | **Above the 80/100 weekly threshold.** |

### Critical-calculation condition

Rechecked the final submitted critical items: Q1–5 and Q14–18 are **10/10 correct after remediation**, including costs in planned stop risk. Values: MES tick USD 1.25, MES move 15 ticks/USD 18.75; MNQ tick USD 0.50 and move USD 7; MGC tick USD 1 and move USD 23; MCL tick USD 1 and move USD 27. Stop-risk totals: Q14 USD 24.50; Q15 USD 25.75 (skip); Q16 USD 23; Q17 USD 24; Q18 USD 26 (skip). Fresh MGC/MCL tick-value checks and MCL USD 27 risk rejection, documented earlier, support remediation beyond merely copying corrections. The later actual-fill P&L arithmetic mistake is preserved and scored; it is not silently presented as a correct first attempt. Critical risk/tick calculation requirement is met on the reviewed corrected set and rechecks, not as a claim of error-free performance throughout the week.

### Next learning step

Proceed to Week 3 fundamental context and observation. Carry forward the arithmetic check: points → ticks → gross dollars → net dollars, with gross cross-checked using points × multiplier. Revisit gross/net, stop-limit and OCO distinctions briefly during future practice. Formal Week 1 validation and the Week 4 Foundation Gate remain separate; this pass does not change live/simulation execution permissions or validate a trading setup.
