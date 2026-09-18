# Week 2 — Contract Specifications and Trade Mathematics

**Status:** In progress; written Parts A–D reviewed and validated after corrections; next: closed-book quiz and platform lab (see REVIEW.md)
**Prepared:** 2026-09-07  
**Schedule:** Four 2-hour evening sessions, 20:00–22:00 America/Toronto  
**Objective:** Calculate exposure, P&L, and planned risk independently of the platform.

Use `notes/contract-math.md` as the reference. Answer in English; French is welcome when clarifying reasoning. Work in small batches for coach feedback. All numerical prices, fees, and execution assumptions in this assignment are fictional; quantities above one are paper arithmetic only.

## Four-session plan

| Session | Work | Time |
|---|---|---:|
| 1 — Monday | Read unit/formula lessons (30m); solve 1–8 (60m); explain mistakes and update notes (30m) | 2h |
| 2 — Tuesday | Read costs and risk (30m); solve 9–20 (75m); journal (15m) | 2h |
| 3 — Thursday | Study contracts/orders (30m); solve 21–25 (30m); platform lab (60m) | 2h |
| 4 — Friday | New mixed practice/rework (75m); closed-book quiz (15m); weekly review and journal (30m) | 2h |

If a session has already passed, continue in this order at the next available study period.

## Bridge from Week 1

Written answers exist, but no formal Week 1 pass is recorded. During this week, clarify exposure versus collateral and offset versus final settlement. Week 1 notes also need later review of exchange versus clearinghouse roles and simulation fill assumptions. Do not mark Week 1 complete solely because Week 2 has begun.

## 25 contract-math problems

For every calculation: show formula, substitution, units, result, and one sentence explaining its meaning. Use the verified specification table in `notes/contract-math.md`. Items marked **critical** require fully correct tick/stop calculations before passing.

### A — Units and contract size

1. **Critical:** Calculate MES tick value from its multiplier and tick size.
  MES multiplier contract unit 5$ -> tick size 0.25 point, tick value = 5$/4 = 1.25$
2. **Critical:** Convert a 3.75-point MES move into ticks and dollars for one contract.
  3*4 = 12, 12 + 3 = 15 ticks total. 15 ticks * 1.25$ = 18.75$
3. **Critical:** Calculate MNQ tick value, then the dollar value of 14 ticks for one contract.
2$ per index point, 0.25 tick size -> 2/4 = 0.5$. 14 ticks * 0.5$ = 7$
4. **Critical:** Calculate MGC tick value, then convert a $2.30/oz move into ticks and dollars for one contract.
10 troy ounces, 0.10$ per ounce -> 10*0.1$ = 1$. 2.3$/oz move is 23 ticks -> 23 * 1$ = 23$
5. **Critical:** Calculate MCL tick value, then convert a $0.27/barrel move into ticks and dollars for one contract.
100 barrel per contract, 0.01$ tick size -> 100*0.01 = 1$ per tick. Move of 0.27$/barrel / 0.01$ =  27 ticks,  27 ticks * 1$/tick = 27$
6. Calculate notional exposure for one MES at 6,000, one MNQ at 20,000, one MGC at 2,500, and one MCL at 75.
MES: 6000 * 5$ * 1 = 30 000$
MNQ: 20 000 * 2$  * 1= 40 000$
MGC: 2500 * 10 * 1= 25 000$
MCL: 75* 100 * 1 = 7500$
7. A hypothetical broker changes MES margin from $1,500 to $2,000. Price stays at 6,000. Calculate notional exposure and one-tick P&L before and after. Explain what changed.
Notional exposure: 6000 * 5$ = 30 000$
one-tick p&l: 5$ index point * 0.25 = 1.25$ per tick 
The notional exposure does not change because the margin requirement increase. The exchange defines the multiplier, while notional exposure depends on price × multiplier × quantity. Margin requirements also involve clearing requirements and broker policies.
8. Is 6,000.10 a valid MES outright limit price on a 0.25-point grid? Give the adjacent valid prices.
   No, MES increases by 0.25. So the next value after 6000 is 6000.25.


### B — P&L from actual fills

For 9–13, the prices are actual fills. Calculate gross P&L and net P&L with hypothetical $2 round-trip commission/fees per contract. Do not add a slippage charge.

Gross PL: Gross long P&L = (exit fill − entry fill) × M × Q  ------- Gross short P&L = (entry fill − exit fill) × M × Q
net PL: Net realized P&L = gross P&L from actual fills − actual commissions and fees

9. Long 1 MES: entry 6,000.00, exit 6,006.25.
Gross PL: (6006.25 - 6000) * 5 * 1 = 31.25$
net PL: 31.25$ - 2$ = 29.25$
10. Short 1 MES: entry 6,010.00, exit 6,013.50.
Gross PL: (6010-6013.5) * 5 * 1 = -17.5$
net PL: -17.5 - 2 = -19.5$
11. Short 2 MNQ: entry 20,000.00, exit 19,992.50. Paper arithmetic only.
Gross PL: (20000-19992.5) * 2 * 2 = 30$
net PL: 30 - 2*2 = 26$
12. Long 1 MGC: entry 2,500.0, exit 2,498.6.
Gross PL: (2498.6-2500) * 10 onces = -14$
net PL: -16$
13. Short 1 MCL: entry 75.00, exit 74.83.
Gross PL: (75 - 74.83) * 100 barils = 17$
net PL: 17 - 2 = 15$

### C — Planned risk and costs

For 14–19 use C = $2 round-trip fees per contract and S = 2 adverse ticks total per contract across entry/exit. Do not treat S as two ticks on each side. Budget = $25. Entry/stop levels are planning references.

14. **Critical:** Long 1 MES at 6,000.00, stop 5,996.00. Calculate stop ticks, price risk, total planned risk, and whether it fits the budget.
Stop ticks: (6000-5996) * 4 = 16 ticks
Price risk: 4 points * 5 = 20$
Total planned risk: 20$ + 2$ + (1.25 * 2) = 24.5
Fit budget: Yes
15. **Critical:** Long 1 MES at 6,000.00, stop 5,995.75. Repeat question 14. If it fails, state the decision without moving the stop.
Stop ticks: (6000 - 5995.75) = 4,25 points. 4.25 / 0.25 = 17 ticks
Price risk: 4.25 / 0,25 * 1,25 = 21.25$
Total planned risk: 21.25$ + 2$ + 2.5$ = 25.75$ 
Fit budget: No, because the total planned risk is greater than the budget.
16. **Critical:** Short 1 MNQ at 20,000.00, stop 20,010.00. Calculate stop ticks and total planned risk.
Stop ticks: (20010-20000) * 4 = 40 ticks
Total planned risk: (40 * 0.5$) + 2$ + (2 * 0.5$) = 23$
17. **Critical:** Long 1 MGC at 2,500.0, stop 2,498.0. Calculate stop ticks and total planned risk.
Stop ticks: (2500 - 2498) * 10 = 20 ticks
Total planned risk: (20 * 1$) + 2$ + (2 * 1$) = 24$
18. **Critical:** Short 1 MCL at 75.00, stop 75.22. Calculate stop ticks, total planned risk, and the budget decision.
Stop ticks: (75.22 - 75) * 100 = 22 ticks
Total planned risk: (22 ticks * 1$) + 2 + (2 * 1$)  = 26$
Fit budget: No, greater than 25$
19. A paper MES scenario has an 8-tick stop. Calculate risk per contract, the risk-based quantity for $25, and the quantity permitted by the academy cap. Does this alone authorize a trade?
Risk per contract: (8 * 1.25$) + 2$ + 2.5$ = 14.50
Risk for 25$: 25$ / 14.5$ = 1.72 contract
Max quantity: 1.72 down to 1 micro
Authorize:Non. Le calcul autorise une quantité selon le budget, mais le trade doit aussi respecter la stratégie et les règles de gestion du risque.
20. An actual long MES fill is 6,000.25; actual exit is 5,995.75; round-trip fees are $2. Initial planned risk was $24.50. Calculate gross P&L, net P&L, and result in R. Explain why you do not subtract another slippage allowance.
Gross PL: (5995.75 - 6000.25) * 5$ = -22.50$
Net PL:-22.5-2$ =  -24.50$
R = -24.50 / 24.50 = -1R
Explain: Slippage is not calculated because the slippage is part of the entry and exit price. 

### D — Spread and order scenarios

21. MES bid is 6,000.00 and ask is 6,000.25. Assume an immediate buy fills at that ask and an immediate sale fills at that bid, both for one contract. With $2 round-trip fees, calculate spread in ticks, gross P&L, and net P&L.
Spread: 6000.25 - 6000 = 0.25 points. 0.25/0.25 = 1 tick
Gross PL: -0.25/0.25 * 1.25 = -1.25
Net PL: -1.25-2 = -3.25 $
22. A paper plan targets an 8-tick MES gain with C = $2 and S = 2 ticks total. Calculate gross target profit, estimated net profit, and costs as a percentage of gross target profit.
Gross target profit: 8 * 1.25 = 10$
Net profit: 10 -2$ - (2*1.25) = 5.5$
Cost % gross target profit: 4.5 / 10 = 0.45 = 45%
23. A long MES entry fills at 6,000.00. Its sell stop triggers at 5,996.00 but fills at 5,995.25. Fees are $2 round trip. Calculate adverse stop slippage in ticks, actual net loss, and excess loss over a plan assuming an exact stop fill plus fees.
Stop slippage ticks: 5996-5995.25 = 0.75. 0.75/0.25 = 3 ticks
Net loss: 6000-5995.25=4.75. 4.75/0.25= 19 ticks. 19 * 1.25= 23.75. -23.75-2= -25.75$
Excess loss:  25.75 - 22 = 3.75$
24. A long MES at 6,000.00 uses a sell stop-limit: trigger 5,996.00, limit 5,995.75. After triggering, available bids jump to 5,994.00 with no fill at or above the limit. Does the exit necessarily fill? Calculate unrealized gross P&L marked at 5,994.00 if the position remains open.
No, because the minimum is 5995.75.
Gross PL: 5994-6000=-6 points. -6 / 0.25 = -24 ticks. -24 * 1.25 = -30$
25. A hypothetical MES long bracket has entry 6,000.00, target 6,006.00, and stop 5,996.00, one contract. Calculate target and stop offsets in ticks. If the target fills exactly, calculate net profit with $2 fees. Explain the intended effect on the OCO stop and what must be checked afterward.
Target offset: (6006-6000 ) / 0.25 = 24 ticks
Stop offset: (6000-5996) / 0.25 = 16 ticks sous l'entrée

> Coach correction, 2026-09-17: reversed the subtraction to express the positive distance. The original `(5996-6000) / 0.25` equals −16 ticks, which is the signed displacement below entry.

Net profit: 24 * 1.25 - 2 = 28$
Explain: The OCO orders aim to set a take profit and a stop loss. This help control the risk. Afterward the trader must check the slippage to know the real profit or loss. When the objective is fulfill, the orders associated to that objective are cancel. Un stop vendeur laissé actif pourrait ensuite ouvrir une position short involontaire s’il s’exécute.
L’objectif a été entièrement exécuté pour un contrat.
La position est flat : zéro contrat.
Le stop lié par OCO est confirmé annulé, sans ordre résiduel associé à ce trade.


## Contract and platform lab — no order submission

1. Record whether Sierra Chart is installed and what simulation/data service is available. The old profile says not installed; current state is unverified.
2. Record the exact dated MES symbol and observation/replay date. Compare relevant expiry volumes, cite the source/time, and justify the active-contract choice. Do not guess it from the current calendar month.
3. Verify tick size, multiplier, expiry, and financial settlement from official product details. Distinguish switching a chart symbol from rolling an open position.
4. With simulation mode and intended account visibly confirmed, prepare the question 25 bracket fields without pressing Buy, Sell, or any submission control. Save evidence of quantity and tick offsets under `journal/screenshots/week-02/`.
5. If the platform is unavailable, draw the order ticket on paper and record `platform evidence pending`; this is preparation, not completion of the platform lab.

Reference: [Sierra Chart Attached Orders](https://www.sierrachart.com/index.php?page=doc/AttachedOrders.html). Platform behavior must be checked for the installed version and selected service.

## Closed-book concept quiz

After the practice and feedback, answer in your own words:

1. Distinguish tick, point, tick value, and multiplier.
2. Distinguish notional exposure, margin, and planned risk-to-stop.
3. Why is planned stop risk not a maximum possible loss?
4. When would subtracting slippage double-count a cost?
5. Distinguish offset, rollover, and final settlement. Why is the third Friday not a universal expiration rule?
6. What can fail with a stop-limit order or a bracket/OCO workflow?
7. How do you select the appropriate contract month for a historical replay?
8. What do you do when the calculated risk-based quantity is zero?

## Weekly review and evidence

- Record each actual study session in the journal's Study Log; do not prefill attendance.
- Add your explanations and examples to the student section of `notes/contract-math.md`.
- Submit calculation attempts in numbered batches, retaining the original errors and corrected reasoning.
- Submit platform evidence or explicitly record what remains pending.
- End with: strongest concept, recurring error, remaining uncertainty, next practice target.

Scoring follows `CURRICULUM.md`: concepts 25, practical lab 35, deliverables 20, journal 10, process/risk 10. Pass requires at least 80/100, all critical tick/stop calculations correct, and no critical safety failure. Remediation uses new equivalent questions; do not count copying a correction as mastery. No score or completion is recorded before reviewing actual evidence.
