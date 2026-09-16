# Week 2 — Contract Specifications and Trade Mathematics

**Prepared:** 2026-09-07  
**Status:** Instructor reference; student explanations and assessment pending  
**Language:** English terminology; coaching may be in French  
**Scope:** Paper calculations and an unsubmitted simulation order ticket. All prices and costs below are hypothetical, in USD.

## 1. Start with the unit

A tick is the minimum permitted price increment for the order being studied. A point is a move of 1.00 in the quoted price. They are not interchangeable.

For these outright futures (not options or calendar spreads):

| Contract | Multiplier / contract unit | Tick size | Tick value, one contract | Value of a 1.00 price move |
|---|---|---|---:|---:|
| MES | $5 per index point | 0.25 index points | $1.25 | $5 |
| MNQ | $2 per index point | 0.25 index points | $0.50 | $2 |
| MGC | 10 troy ounces | $0.10 per ounce | $1.00 | $10 |
| MCL | 100 barrels | $0.01 per barrel | $1.00 | $100 |

Checked against CME sources on 2026-09-07: [Micro equity futures FAQ](https://www.cmegroup.com/articles/faqs/micro-e-mini-equity-index-futures-frequently-asked-questions.html), [Micro Gold overview](https://www.cmegroup.com/education/lessons/micro-gold-and-micro-silver-futures-product-overview), [Micro WTI FAQ](https://www.cmegroup.com/education/articles-and-reports/micro-wti-crude-oil-futures-faq). The older WTI FAQ contains explicitly dated margin figures: do not use those as current margin requirements.

For MES, 1 point = 4 ticks. Write the unit at every step:

```text
0.25 points/tick × $5/point = $1.25/tick
3.00 points ÷ 0.25 points/tick = 12 ticks
12 ticks × $1.25/tick = $15 per contract
```

## 2. Three different dollar amounts

**Notional exposure:** futures price × multiplier × contracts. At a hypothetical MES price of 6,000, one contract represents $30,000 of exposure.

**Margin:** collateral required to open/maintain a position. It does not change the contract multiplier or cap losses. Initial and maintenance requirements can change; broker intraday policies require separate verification. [CME margin lesson](https://www.cmegroup.com/education/courses/introduction-to-futures/margin-know-what-is-needed)

**Planned risk-to-stop:** loss calculated to the initial stop, plus estimated costs and adverse execution. This is a planning amount, not a guaranteed maximum loss. A worse fill or an unfilled protective order can produce a larger loss.

## 3. Formula card

Let Q be contract quantity; M the dollar value of a 1.00 price move; T the tick size; V the tick value. C is commission plus fees for a round trip, per contract. S is the total adverse slippage allowance in ticks across entry and exit, per contract.

```text
V = T × M
Distance in ticks = abs(price B − price A) ÷ T
Gross long P&L = (exit fill − entry fill) × M × Q
Gross short P&L = (entry fill − exit fill) × M × Q
Planned risk = [abs(planned entry − initial stop) × M + C + S × V] × Q
Net realized P&L = gross P&L from actual fills − actual commissions and fees
Net estimated P&L from reference prices = gross reference P&L − Q × (C + S × V)
Risk-based quantity = floor(risk budget ÷ planned risk per contract)
Result in R = net realized P&L ÷ initial planned risk dollars
```

Slippage and spread are already reflected when P&L uses actual entry/exit fills. Do not subtract them again. When using reference prices, explain what the execution allowance includes so spread is not counted twice.

The academy additionally caps execution practice at one Micro. A risk-based quantity below one means skip; a result above one does not lift the one-Micro cap. Do not move the invalidation merely to fit the $25 training budget. This calculation is not a complete permission-to-trade check; see `RISK-MANAGEMENT.md` and the current playbook status.

## 4. Worked examples

### MES — Long, stop, and estimated costs

Hypothetical entry 6,000.00; initial stop 5,996.00; Q = 1; C = $2.00; S = 2 ticks total.

- Distance: 4.00 points / 0.25 = 16 ticks.
- Price risk: 16 × $1.25 = $20.00.
- Allowance: $2.00 + 2 × $1.25 = $4.50.
- Planned risk: $24.50. It fits the $25 arithmetic limit.
- If the actual exit is 5,995.50 and the actual entry is 6,000.00: gross loss = $22.50; with $2 fees, net loss = $24.50. Do not subtract another slippage allowance.

### MNQ — Short P&L

Actual entry fill 20,000.00, actual exit fill 19,992.50, Q = 1: favorable movement = 7.50 points = 30 ticks. Gross profit = 7.50 × $2 = $15. With hypothetical $2 round-trip fees, net profit = $13.

### MGC — Stop distance

Long reference entry 2,500.0, stop 2,498.5, Q = 1: distance = $1.50/oz = 15 ticks; price risk = $15. With C = $2 and S = 2 ticks total, planned risk = $19. Notional exposure at entry = 2,500 × 10 = $25,000.

### MCL — Short P&L

Actual entry fill 75.00, actual exit fill 74.82, Q = 1: favorable movement = $0.18/barrel = 18 ticks. Gross profit = 0.18 × 100 = $18; with $2 round-trip fees, net profit = $16. Notional exposure at entry = 75 × 100 = $7,500.

## 5. Contract identity, expiration, and rollover

Month codes: Jan F, Feb G, Mar H, Apr J, May K, Jun M, Jul N, Aug Q, Sep U, Oct V, Nov X, Dec Z. `MESU26` illustrates MES September 2026; the exact platform symbol format depends on its data service. A month code exists for every month, but each product has its own listed months. [CME month codes](https://www.cmegroup.com/month-codes.html)

Do not infer the active contract from today's month alone. Compare dated volume in the relevant expiries and check the product calendar. For replay, do this for the historical session. Record the contract, observation date, volume evidence, last trading date, and applicable broker deadline.

Offsetting closes a position with an opposite transaction in the same contract and quantity. Rolling closes one expiry and opens another. Final settlement resolves the remaining obligation under the contract rules; it can be financial or physical. Expiration is product-specific, not universally the third Friday. [CME expiration and rollover](https://www.cmegroup.com/education/courses/introduction-to-futures/understanding-futures-expiration-contract-roll)

MCL is financially settled, unlike physically delivered CL. This corrects the idea that every commodity future requires physical delivery. [CME Micro WTI FAQ](https://www.cmegroup.com/education/articles-and-reports/micro-wti-crude-oil-futures-faq)

## 6. Order vocabulary

| Term | Meaning | Limitation to explain |
|---|---|---|
| Market | Requests execution against available liquidity | The displayed price is not guaranteed |
| Limit | Buy at the limit or lower; sell at the limit or higher | May remain unfilled, including after a touch |
| Stop | Activates when its trigger condition is met | Trigger price is not a guaranteed fill |
| Stop-limit | Activates a limit order | Can remain unfilled while the market moves away |

CME Globex uses protection mechanisms for market/stop orders; exact supported types and trigger behavior depend on the product and routing. Read the platform mapping before use. [CME futures order types](https://www.cmegroup.com/education/courses/futures-trading-mechanics-and-regulation/futures-order-types)

A bracket associates an entry with protective and profit-taking orders. OCO links exit orders so execution of one causes cancellation of its counterpart under the service's rules. Confirm quantity, parent/child behavior, and whether management occurs locally or on a server. A bracket does not guarantee a maximum loss. [Sierra Chart Attached Orders](https://www.sierrachart.com/index.php?page=doc/AttachedOrders.html)

## 7. Student notes — complete after the lesson

1. Explain point versus tick in your own words:
2. Explain notional versus margin versus planned risk:
3. Show a new MES long example and a new MES short example:
4. Explain how you avoid double-counting execution costs:
5. Record one mistake, its cause, and the check that prevents it:
