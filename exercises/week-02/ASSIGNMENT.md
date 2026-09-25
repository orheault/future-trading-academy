# Week 2 — Contract Specifications and Trade Mathematics

**Status:** Passed after remediation — 85/100, 2026-09-24. Written work, platform preparation, quiz, notes, reflection and Study Log reviewed; final rubric and evidence limitations in REVIEW.md. This is not an unassisted perfect score or trade authorization.
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
Stop offset: (5996 - 6000) / 0.25 = -16 ticks, sous l'entrée

> Coach correction, 2026-09-17: reversed the subtraction to express the positive distance. The original `(5996-6000) / 0.25` equals −16 ticks, which is the signed displacement below entry.

Net profit: 24 * 1.25 - 2 = 28$
Explain: The OCO orders aim to set a take profit and a stop loss. This help control the risk. Afterward the trader must check the slippage to know the real profit or loss. When the objective is fulfill, the orders associated to that objective are cancel. Un stop vendeur laissé actif pourrait ensuite ouvrir une position short involontaire s’il s’exécute.
L’objectif a été entièrement exécuté pour un contrat.
La position est flat : zéro contrat.
Le stop lié par OCO est confirmé annulé, sans ordre résiduel associé à ce trade.


## Contract and platform lab — no order submission

1. Record whether Sierra Chart is installed and what simulation/data service is available.

   Coach evidence record, 2026-09-18 — Question 1 complete: installed (screenshot from 2026-09-03); student confirms current service `SC Data`, simulation indicator `[Sim]`, selected account `Sim1` in the Trade Window, and `Delayed` on the chart. Current settings are student-reported; no orders submitted by the coach.

2. Record the exact dated MES symbol and observation/replay date. Compare relevant expiry volumes, cite the source/time, and justify the active-contract choice. Do not guess it from the current calendar month.

   Coach evidence record, 2026-09-18 — Question 2 complete: student reports chart symbol `MESZ26-CME` (MES December 2026) and confirms observation of the current delayed market, not historical replay. The contract comparison below uses the completed 2026-09-17 daily session, reviewed on 2026-09-18, because current quote Daily Volume was zero.

   Historical comparison (same-session fallback), screenshots reviewed 2026-09-18:

   | Contract | Selected daily session | Volume (contracts) | Evidence under journal/screenshots/week-02/ |
   |---|---|---:|---|
   | MESU26-CME — September 2026 | 2026-09-17 | 123,498 | 2026-09-17_MESU26_daily-volume.png |
   | MESZ26-CME — December 2026 | 2026-09-17 | 1,014,522 | 2026-09-17_MESZ26_daily-volume.png |

   Coach interpretation: December shows approximately 8.21 times September's volume, supporting December as the more actively traded of these two expiries for that session. This is historical daily-bar evidence, not current-session volume or a comparison of every listed expiry. The student confirms all-expiry volume aggregation is No and, on 2026-09-18, Continuous Contract = None on both charts. Settings are student-reported; the selected dates and volumes are visible in the saved screenshots. Contract-specific comparison accepted for this exercise.

3. Verify tick size, multiplier, expiry, and financial settlement from official product details. Distinguish switching a chart symbol from rolling an open position.
Tick size: Outright: 0.25 index points = $1.25 
multiplier: $5 x S&P 500 Index
expiry: last trade: 18 Dec 2026
settlement: Financially Settled

   Coach review, 2026-09-22: the four recorded specifications are correct for MESZ26: outright tick 0.25 index points / USD 1.25, multiplier USD 5 per index point, December 18, 2026 expiration under the third-Friday rule, and financial settlement. Reference: [CME Rulebook, Chapter 353](https://www.cmegroup.com/rulebook/CME/IV/350/353/353.pdf), checked 2026-09-22. The final part is unanswered: explain in your own words how changing the chart symbol differs from rolling an open position. Question 3 remains partially complete until that explanation is provided. Student answers above are preserved.

   Student follow-up in chat, 2026-09-22: “Dans ce cas, il serait nécessaire d'effectuer une transaction de type rollover. Cette transaction ferme la position en septembre et ouvre une position pour décembre”

   Coach final review, 2026-09-22 — Question 3 complete after feedback: rollover explanation accepted. Coach clarification: changing the chart symbol alone leaves the existing position on its original expiry; rolling requires closing that position and opening the later expiry. This clarification is instructor-provided, not an additional student quotation. Platform lab questions 1–4 are now complete; the closed-book quiz remains pending.

4. With simulation mode and intended account visibly confirmed, prepare the question 25 bracket fields without pressing Buy, Sell, or any submission control. Save evidence of quantity and tick offsets under `journal/screenshots/week-02/`.

   Coach review, 2026-09-22: screenshots saved as `2026-09-22_bracket-main.png` and `2026-09-22_bracket-targets-stop-limit.png` in the evidence directory. Visible: `[Sim]`, `Sim1`, Flat, MESZ26-CME, parent Limit 6,000 and quantity 1, Use Attached Orders enabled, Target 1 Limit 24 ticks / quantity 1, Stop 1 Stop Limit 16 ticks / quantity 1 with OCO Group 1 selected. Distances accepted. The original instructions did not specify the stop subtype; coach now specifies `Stop: Stop` for this simulation preparation exercise and explains the non-fill risk of Stop Limit. Final configuration review pending an updated stop screenshot and confirmation that Target 1 also uses OCO Group 1. Flat alone does not prove absence of pending orders or that no order was submitted. No submission is required or authorized by this exercise.

   Follow-up evidence, 2026-09-22: `2026-09-22_bracket-targets-stop.png` visibly confirms Stop 1 now uses `Stop: Stop`, offset 16 ticks, quantity 1, OCO Group 1. Stop configuration accepted. Only confirmation of Target 1's OCO Group 1 remains for this configuration review; no order submission requested.

   Final configuration review, 2026-09-22 — Question 4 complete: `2026-09-22_bracket-target-selected.png` visibly confirms Target 1 uses `Target: Limit`, offset 24 ticks, quantity 1, OCO Group 1. Together with the corrected stop screenshot and Main-tab evidence, the required bracket preparation is accepted. This validates ticket configuration only; it does not demonstrate execution or actual OCO cancellation. No order submission is requested. Question 3 remains outstanding.

5. If the platform is unavailable, draw the order ticket on paper and record `platform evidence pending`; this is preparation, not completion of the platform lab.

Reference: [Sierra Chart Attached Orders](https://www.sierrachart.com/index.php?page=doc/AttachedOrders.html). Platform behavior must be checked for the installed version and selected service.

## Closed-book concept quiz

After the practice and feedback, answer in your own words:

1. Distinguish tick, point, tick value, and multiplier.

   Student answer in chat, 2026-09-22: “Un tick est la plus petit incrément de prix. La grosseur du tick dicte le nombre de tick formant 1 point. Le point, tick et multiplicateur son défini par l'exchange. Le multiplicateur est la valeur du point. Par exemple, un point du mes vaut 5$, un tick vaut 1.25$.”

   Coach review: accepted with clarification. The student correctly defines the minimum increment and multiplier and supplies MES point/tick dollar values. A point is one unit of the quoted price; MES tick size is 0.25 point, so four ticks form one point. Those explicit point-unit and tick-size details are instructor additions, not verbatim student evidence. Dollar values are USD per contract.

2. Distinguish notional exposure, margin, and planned risk-to-stop.

   Student answer in chat, 2026-09-22: “L'exposition notionnelle est la valeur total du produit sous jacen du contrat. La marge sont les montants requis pour ouvrir et maintenir une position. Le risque planifié jusqu'au stop représente la perte en tick comprenant le slippage estimé ainsi que les frais de trading. La marge ne représente pas la perte maximal possible. La marge représente le montant requis pour effectuer des opérations. La perte maximal dépend du montant dans compte par rapport à la valeur notionnelle.”

   Coach review: partially correct; remediation pending. Notional exposure and margin descriptions are broadly correct. Planned monetary risk requires converting stop/slippage ticks into dollars before adding fees, accounting for quantity. The account balance relative to notional exposure describes leverage, not a maximum loss. Futures losses can exceed deposited funds; realized loss depends on price movement through actual exit, multiplier, quantity, and costs. Reference checked 2026-09-22: https://www.nfa.futures.org/investors/investor-resources/files/investor-best-practices.html. Follow-up hypothetical: an account starts with USD 500 and a closed position incurs USD 650 net loss; determine the resulting balance and explain whether the original balance capped the loss. No trade is requested.

   Student remediation answer in chat, 2026-09-22: “le nouveau solde est de -150$. Les 500$ n'ont pas limité la perte car tout largent est perdu.”

   Coach review: balance/loss-cap remediation accepted. USD 500 − USD 650 = −USD 150; loss exceeds the initial funds by USD 150, rather than merely exhausting them. Question 2 accepted after feedback; the monetary-risk unit conversion remains instructor-supplied clarification. Continue to question 3; no overall quiz score assigned.

3. Why is planned stop risk not a maximum possible loss?

   Student answer in chat, 2026-09-23: “Plusieurs cas peuvent survenir causant une plus grande perte que le risque planifié. Le slipage peut excéder la valeur planifier. La vitesse d'exécution du marché peut aussi causer une plus grosse perte.”

   Coach review: accepted. The student identifies that actual adverse slippage can exceed the planned allowance. Clarify the second sentence as rapid price movement and/or execution delay: the stop trigger price does not guarantee the actual fill price. This mechanism clarification is instructor-provided. Continue to quiz question 4.

4. When would subtracting slippage double-count a cost?

   Student answer in chat, 2026-09-23: “Dans ce cas, je ne dois pas soustraire une provision de slippage. La valeur du slippage est inclu dans le prix de sortie.”

   Coach review: accepted. Student correctly rejects an additional slippage provision when actual fills are used. Clarification: actual entry and exit fills both incorporate any slippage at their respective execution; subtract actual commissions/fees from gross fill-based P&L, without another slippage deduction. Continue to quiz question 5.

5. Distinguish offset, rollover, and final settlement. Why is the third Friday not a universal expiration rule?

   Student answer in chat, 2026-09-23: “Offset est le principe de fermer une position puis de passer a l'étape de règlement final. Le but de ces deux étapes est de recevoir le produit sous jacen. Le rollover permet de fermer une position et d'ouvrir une autre position dans une autre échéance. Lors du rollover, il n'y a pas de settlement final pour recevoir le produit sous jacen du contrat.”

   Coach review: remediation required. Rollover close/reopen mechanism is correct. Offset closes the position through an equal opposite transaction in the same contract/expiry; it does not lead that closed position to expiry delivery. Final settlement applies to positions held to expiry and follows contract-specific cash or physical settlement rules; MES is cash-settled. Closing/rolling realizes P&L, and avoiding expiry settlement does not mean avoiding all cash flows or daily settlement. Third-Friday explanation is missing; expiry rules are product-specific and require official specifications/calendar. Sources checked 2026-09-23: CME Understanding Futures Expiration & Contract Roll and CME Rulebook Chapter 353. Follow-up: explain whether selling one previously purchased December MES before expiry leaves any position to settle at expiry, whether holding MES to expiry delivers shares, and why the same expiry rule cannot be assumed for gold or crude oil. Student response pending.

   Student remediation answers in chat, 2026-09-23:
   - “1. Il ne reste plus de position à régler étant donné qu'elle a été offset.”
   - “2. Lorsque la date d'expiration est arrivé et que j'ai des positions ouvertes, le règlement sera financier pour le MES.”
   - “3. Je dois consulter la page d'information du contrat sur l'exchange. Dans ce cas ci CME.”

   Coach review: all three follow-up answers accepted. Student correctly recognizes no remaining expiry position after a full offset, cash settlement for MES held to expiry, and official contract specifications as the source for expiry rules. Question 5 accepted after remediation; continue to question 6. No overall score assigned.

6. What can fail with a stop-limit order or a bracket/OCO workflow?

   Student answers to the three chat prompts, 2026-09-23:
   - “1. Je ne suis pas certain.”
   - “2. Si mon objectif est exécuté, mais le stop au groupe oco reste actif, le risque est qu'une position de vente soit ouverte si le prix atteint la valeur du stop.”
   - “3. Après exécution, je dois vérifier que le stop loss et take profit sont bien fermés. Ensuite je vérifie les valeurs d'exécution pour vérifier le slippage.”

   Coach review: partially correct, remediation pending. The orphan sell stop can open an unintended short after a long has fully exited. Checking executions/slippage is appropriate. Make status checks precise: target fully Filled for the intended quantity, position Flat/zero, linked stop confirmed Canceled and no residual orders associated with the trade. Stop-limit explanation supplied by coach: trigger activates a limit order; a sell limit cannot execute below its limit, so a market drop can leave the long open. Teaching example: sell stop trigger 5,996.00 / limit 5,995.75, with best available bid 5,995.00 after triggering. Source: Sierra Chart Order Types, checked 2026-09-23. Follow-up uses a different limit (6,099.50) and best bid (6,099.00) after triggering; explain whether the stop-limit can sell there, what happens to the position, and the position/order statuses to check after a complete target fill.

   Student remediation answers in chat, 2026-09-23:
   - “1. Il ne peut pas vendre au prix de 9099.00, car la limit est de 6099.50. La position restera ouverte.”
   - “2. Je dois vérifier que tous les contrats sont fermés, entièrement exécuté. Et qu'il n'y a plus d'ordre ouverte associé à l'objectif. Le stop doit être fermé.”

   Coach review: accepted after remediation and terminology clarification. Interpret `9099.00` as a transcription typo for the prompt's `6099.00`, because the stated limit and non-fill/open-position reasoning fit that scenario; the literal 9099.00 would be above the sell limit. Student recognizes that no fill leaves the position open, and checks full closure and absence of residual orders. Coach specifies the exact statuses: target Filled for full quantity, position Flat/zero, stop Canceled. These exact status terms remain instructor-provided clarification. Continue to question 7.

7. How do you select the appropriate contract month for a historical replay?

   Student answer in chat, 2026-09-23: “J'appuis sur FIle/Find Symbol. Je dois prendre le symbole auquel il y a plus de volume comparé à l'échéance suivant.”

   Coach review: partially complete. Student correctly proposes comparing volume between relevant expiries, but does not specify the historical comparison date or time basis. Follow-up asks whether, for a replay of 2026-09-17, the comparison should use today's volumes or historical volumes around the replay date, and why. For a selection decision before that replay session opens, use a completed preceding session or information already available at that time, avoiding future information. Exact dated symbol and comparison source/time should be recorded. Question 7 remains pending; the timing clarification above is instructor guidance, not student evidence.

   Student follow-up in chat, 2026-09-23: “Il faut vérifier la période historique rejouée.”

   Coach review: question 7 accepted after prompting. Combined with the initial volume-comparison answer, the student identifies the relevant historical period rather than current volume. Coach clarification: compare expiries on the same historical time basis; if choosing before the replay session opens, use the preceding completed session or other information already available then, not that session's future closing volume. The no-look-ahead detail is instructor-provided, not independently stated by the student. Continue to question 8.

8. What do you do when the calculated risk-based quantity is zero?

   Student answer in chat, 2026-09-23: “Je ne prend pas le trade, étant donnée que le risque planifié dépasse le budget. C'est important.”

   Coach review: correct no-trade decision for the USD 25 budget / USD 28 risk-per-contract scenario. The second part of the chat prompt remains unanswered: may the stop be moved closer solely to fit the budget, and why? Record the decision as accepted; final Q8 follow-up pending. No full-quiz or weekly completion assigned.

   Student follow-up in chat, 2026-09-23: “Je ne peux pas rapprocher le stop, car cela va à l'encontre de ma stratégie de trading. Rapprocher le stop m'expose à un risque de me faire sortir, du au price action.”

   Coach review: question 8 accepted. Student correctly declines an unaffordable contract and rejects moving the stop solely to force it into the budget because that changes the strategy's setup. This does not prohibit a different stop justified independently by the strategy. All eight quiz questions have now been reviewed and accepted, with corrections/prompts preserved; this is not an unassisted perfect score. Remaining weekly evidence and final assessment are still pending.

## Weekly review and evidence

Student weekly reflection submitted in chat, 2026-09-24:
1. Strongest concept: “Je comprends le risque calculé et son importance de bien respecter notre plan de match.”
2. Recurring error: “Mon erreur récurrente sont les petites coquilles lors des calculs, faussant mes résultats.”
3. Remaining uncertainty: “Je pense que tout est clair”
4. Next interest: “j'ai hate de définir une stratégie de trading dans le future”

Coach response: reflection received. Respect for planned risk is a strength; arithmetic errors need a repeatable check, not just more care. Recommended immediate practice target: write points, ticks, gross dollars and net dollars on separate lines, then cross-check points × multiplier against ticks × tick value. Strategy design remains the student's longer-term interest; the curriculum's formal setup specification is Week 13, with Week 3 covering fundamental context. Reported clarity is self-assessment, not an independent mastery score. Study Log review found missing A14:A22 identifiers, B14:B19 dates and I15/I21/I22 durations; complete only from actual session records, labeling uncertainty rather than inventing entries.

- Record each actual study session in the journal's Study Log; do not prefill attendance.
- Add your explanations and examples to the student section of `notes/contract-math.md`.
- Submit calculation attempts in numbered batches, retaining the original errors and corrected reasoning.
- Submit platform evidence or explicitly record what remains pending.
- End with: strongest concept, recurring error, remaining uncertainty, next practice target.

Scoring follows `CURRICULUM.md`: concepts 25, practical lab 35, deliverables 20, journal 10, process/risk 10. Pass requires at least 80/100, all critical tick/stop calculations correct, and no critical safety failure. Remediation uses new equivalent questions; do not count copying a correction as mastery. No score or completion is recorded before reviewing actual evidence.
