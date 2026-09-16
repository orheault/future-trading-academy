# Week 1 — Futures Foundations (Corrected Notes)

**Reviewed:** 2026-09-15
**Status:** Coach-corrected study reference; not a new student submission or a passed assessment.
**Original:** [Unedited notes](archive/week-01-futures-foundations.original-2026-09-15.md)

The English below corrects terminology and grammar. French coach notes explain the main conceptual changes. All numerical examples are hypothetical, in USD; none is a current margin quote. Model answers are intentionally concise: the assignment still asks for your own 100–200-word explanations in Part C.

## CFTC and market participants

Futures markets allow participants to transfer or assume price risk. Hedgers and speculators describe economic roles; commercial and institutional describe types of participants. These categories can overlap.

The CFTC is a U.S. federal regulator. NFA is a self-regulatory organization, not another government agency. Registration requirements depend on the activity and legal status. In the U.S. framework, FCMs and IBs generally require CFTC registration, subject to exemptions; registered FCMs/IBs must be NFA members. An IB does not hold customer trading funds. Registration does not guarantee profitability or solvency. Sources: [CFTC intermediaries](https://www.cftc.gov/IndustryOversight/Intermediaries/FCMs/fcmib), [NFA registration](https://www.nfa.futures.org/registration-membership/).

> Correction : « Handling customer funds → register to NFA » était trop général. Il faut distinguer le rôle, l'inscription réglementaire et l'entité qui détient les fonds. Ces notes décrivent le cadre américain ; elles ne valident pas l'admissibilité d'un courtier pour ton compte canadien.

## Futures contracts and price discovery

A futures contract is a standardized, exchange-traded agreement creating obligations for a future settlement. Specifications identify the underlying, quantity or multiplier, quotation, tick size, listed months, trading schedule, and settlement procedure. Physical-delivery contracts also specify applicable quality and delivery arrangements.

Price discovery is the ongoing interaction of bids, offers, and transactions. It does not produce one permanent or objectively correct price. [CME contract definition](https://www.cmegroup.com/education/courses/introduction-to-futures/definition-of-a-futures-contract)

## Trading codes

| Month | Code | Month | Code |
|---|---|---|---|
| January | F | July | N |
| February | G | August | Q |
| March | H | September | U |
| April | J | October | V |
| May | K | November | X |
| June | M | December | Z |

Symbols combine a product root, contract month, and year; year digits and service suffixes depend on the platform. Example: `ESH26` denotes the March 2026 E-mini S&P 500 contract in a common shorthand. [CME month codes](https://www.cmegroup.com/month-codes.html)

> Correction : `ESF9` n'était pas un bon exemple de contrat ES standard. Les futures ES ont des échéances trimestrielles H, M, U et Z. Le code F existe, mais cela ne signifie pas que chaque produit possède une échéance de janvier. Ne confonds pas les mois des futures avec les expirations d'options.

ES has a $50-per-point multiplier and a 0.25-point outright tick worth $12.50. It is financially settled. [CME E-mini FAQ](https://www.cmegroup.com/trading/equity-index/eminifaq.html)

## Expiration, offset, rollover, and settlement

- **Offset:** close a long by selling, or a short by buying, the same contract and quantity.
- **Rollover:** close one expiry and open another, usually later. Changing the chart symbol does not roll a position.
- **Final settlement:** resolve the remaining contract obligation through cash settlement or physical delivery under its rules.
- **Expiration:** product-specific; the third Friday is not a universal rule. Check last trading and applicable delivery/notice dates.

Cash settlement uses a final reference price without exchanging the underlying physical asset. Physical delivery follows contract delivery procedures, which may involve documents or warehouse arrangements rather than an immediate shipment to the trader. [CME expiration and rollover](https://www.cmegroup.com/education/courses/introduction-to-futures/understanding-futures-expiration-contract-roll)

> Correction : clôturer une position n'est pas du « cash settlement ». Et « settlement = buy the underlying » est incorrect : les obligations dépendent du contrat et du sens de la position. Le règlement quotidien des gains/pertes est encore une autre notion.

## Ticks, contract size, and notional exposure

| Product | Contract unit / multiplier | One outright tick | Tick value |
|---|---|---|---:|
| ES | $50 per index point | 0.25 points | $12.50 |
| MES | $5 per index point | 0.25 points | $1.25 |
| CL | 1,000 barrels | $0.01/barrel | $10 |
| MCL | 100 barrels | $0.01/barrel | $1 |

Sources: [CME E-mini FAQ](https://www.cmegroup.com/trading/equity-index/eminifaq.html), [Micro equity FAQ](https://www.cmegroup.com/articles/faqs/micro-e-mini-equity-index-futures-frequently-asked-questions.html), [Micro WTI FAQ](https://www.cmegroup.com/education/articles-and-reports/micro-wti-crude-oil-futures-faq).

GC represents 100 troy ounces. At a hypothetical futures price of $1,000/oz, one contract has $100,000 of notional exposure. [CME Gold](https://www.cmegroup.com/markets/metals/precious/gold-futures.html)

Notional exposure = futures price × contract unit/multiplier × quantity.

For one CL at $54/barrel: $54/barrel × 1,000 barrels = $54,000. The 1,000 is a number of barrels, not $1,000. Use the futures contract price, which can differ from the spot price.

At a hypothetical MES price of 6,000, one MES represents $30,000; its price sensitivity remains $5 per point. Notional exposure is neither the margin requirement nor the planned loss at a stop.

## Price limits and price banding

Price limits restrict permitted trading prices and can interact with trading halts. Price banding checks orders against an allowable range around a reference price. Neither guarantees an exit fill or caps an individual trader's loss.

> Correction : « downside 7%, 13%, 20%; upside 7% » ne suffit pas comme règle opérationnelle. L'application dépend du produit, de la séance, de l'heure et du prix de référence. Vérifie la règle du contrat concerné et son calendrier ; ne généralise pas une fiche à tous les indices.

Sources: [CME price limits](https://www.cmegroup.com/trading/price-limits.html), [CME safeguards](https://www.cmegroup.com/content/dam/cmegroup/education/files/cme-clearing-risk-management-and-financial-safeguards.pdf).

## Mark-to-market and margin

Mark-to-market values positions at settlement prices and transfers gains/losses through cash debits/credits. It changes account equity; it is not simply a recalculation of the required margin. Clearing can involve multiple settlement cycles. [CME clearing](https://www.cmegroup.com/education/courses/clearing/what-is-clearing)

Hypothetical example, with no other account activity:

- Starting equity: $10,000; required initial margin: $10,000.
- Required maintenance margin: $8,000.
- Mark-to-market loss: $2,500.
- New equity: $7,500, below maintenance.
- Restoring equity to $10,000 would require $2,500, assuming unchanged requirements. Broker policy may instead require reduction/liquidation; do not assume time to deposit funds.

Futures margin is collateral, not a loan used to purchase the full underlying asset.

- **Initial margin:** requirement to initiate a position.
- **Maintenance margin:** minimum equity requirement to maintain it.
- **Intraday margin:** broker-specific terms that may apply during defined hours.
- **Overnight margin:** applicable holding requirements after the broker's cutoff; not merely a small surcharge at night.

Requirements can change. Lower margin does not make a contract's dollar-per-tick sensitivity smaller. [CME margin lesson](https://www.cmegroup.com/education/courses/introduction-to-futures/margin-know-what-is-needed)

## Calculating profit, loss, and planned risk

For quantity Q and dollar multiplier M:

```text
Tick value = tick size × M
Long gross P&L = (exit fill − entry fill) × M × Q
Short gross P&L = (entry fill − exit fill) × M × Q
Net P&L = gross P&L from actual fills − commissions and fees
Planned risk = |planned entry − stop| × M × Q + estimated costs/slippage
```

A hypothetical long CL from $54.00 to $54.03 gains 3 ticks × $10 = $30 gross. Do not confuse contract notional value with P&L. [CME P&L lesson](https://www.cmegroup.com/education/courses/introduction-to-futures/calculating-futures-contract-profit-or-loss)

> Rappel de semaine 2 : points × dollars/point, ou ticks × dollars/tick. Le risque est un montant positif auquel on ajoute les coûts. Le résultat net porte un signe. Les prix d'exécution réels intègrent déjà le slippage : ne le soustrais pas deux fois.

## Part C — Corrected model answers

### 1. Why do futures markets exist?

They support price discovery and transfer price risk. Your farmer example is useful: selling crop futures can help offset falling cash-market prices. A buyer needing the commodity later may buy futures against rising prices. The hedge does not necessarily involve delivery through the futures contract or guarantee the exact eventual cash-sale price. [CME hedgers](https://www.cmegroup.com/education/courses/introduction-to-futures/understanding-the-role-of-hedgers)

### 2. What is the economic difference between a hedger and a speculator?

A hedger reduces an existing or anticipated business/investment exposure. A speculator deliberately assumes market risk seeking profit. A hedge can require buying or selling. Your stock-portfolio example describes a short hedge, but its size depends on contract exposure and portfolio sensitivity; one cannot simply sell an arbitrary dollar amount of ES. [CME hedgers](https://www.cmegroup.com/education/courses/introduction-to-futures/understanding-the-role-of-hedgers)

### 3. Why is futures margin not the maximum amount at risk?

Margin is collateral. Loss depends on adverse price movement, multiplier, quantity, and costs. A stop can fill worse than planned, and losses can exceed the deposit. [CFTC futures basics](https://www.cftc.gov/LearnAndProtect/AdvisoriesAndArticles/FuturesMarketBasics/index.htm)

### 4. What does the clearinghouse do?

It acts as central counterparty and manages obligations through margin, settlement, and default procedures. Order matching belongs to the trading venue's execution system. Clearing reduces counterparty risk; it does not remove market losses. [CME clearing](https://www.cmegroup.com/education/courses/clearing/what-is-clearing)

### 5. Why can a $10,000 account have much larger exposure?

The collateral requirement can be below the contract's notional value. For example, one MES at 6,000 represents $30,000. Account equity does not change that multiplier. This arithmetic does not establish current margin eligibility or justify taking the position. See the margin and notional sections above.

### 6. Cash settlement versus physical delivery?

Cash settlement resolves the final obligation financially. Physical delivery follows the contract's delivery rules. Closing the position before expiry is offsetting, a separate action. See the expiration section above.

### 7. Why know the month and expiration process?

To identify the actual contract, track liquidity migration, and avoid unintended expiry obligations. Not every contract is physically delivered. Check the product's dates and the broker's potentially earlier deadline. See the expiration section above.

### 8. What does “only risk capital” mean personally?

Your principle is correct: only money you can afford to lose. A clearer formulation is money whose loss would not compromise essential expenses, emergency reserves, debt obligations, or other essential goals. Your actual capacity still needs your own assessment; a stated $10,000 amount alone does not establish it. [CFTC futures basics](https://www.cftc.gov/LearnAndProtect/AdvisoriesAndArticles/FuturesMarketBasics/index.htm)

## Part D — Corrected ecosystem map

```text
Trader uses platform/data to send orders
    → IB (if used) / FCM and execution route → Exchange matching system
Executed trades → Clearinghouse, through clearing members
Customer collateral/account records → FCM
Regulatory oversight surrounds these relationships; it is not an order-routing step.
```

This is a simplified functional map. A customer can deal directly with an FCM; not every FCM is itself a clearing member. Platform, routing, and data services may be separate providers.

| Participant | Role | Does not guarantee | Question before opening an account |
|---|---|---|---|
| Trader | Makes and manages trading decisions; may use automation | Profitability or disciplined behavior | Can I sustain the schedule and mental workload? |
| Introducing broker | Solicits/accepts orders and introduces business; does not hold customer trading funds | Profit or best execution on every order | Which legal entity and FCM will serve my account? |
| FCM | Carries accounts, handles collateral, and arranges clearing access | Profits or immunity from failure | What are its margin, liquidation, and service policies? |
| Exchange | Lists standardized contracts and operates a matching venue | A fill at my preferred price | Where are current specifications, hours, and expiry dates? |
| Clearinghouse | Central counterparty managing settlement obligations | Protection against trading losses | Who clears ES? CME Clearing. |
| Platform/data service | Displays data and provides order-entry tools | Perfect data, uninterrupted access, or custody of funds | Which data/routing services are supported, and what happens on disconnect? |
| CFTC / NFA | Government regulation / industry self-regulation within their respective mandates | Solvency or profitability | What is the firm's exact registration status and disciplinary record? |

Sources: [CFTC FCM/IB roles](https://www.cftc.gov/IndustryOversight/Intermediaries/FCMs/fcmib), [CME clearing](https://www.cmegroup.com/education/courses/clearing/what-is-clearing), [NFA investor resources](https://www.nfa.futures.org/investors/index.html).

> Correction : « certains traders sont des algorithmes » est vrai, mais ne répondait pas à « what it does not guarantee ». Pour le courtier, vérifie l'entité juridique et ses autorisations plutôt que de supposer qu'un site ou un logiciel prouve son statut.

## Part F — Quiz correction

| # | Assessment of original answer | Corrected answer / precision |
|---:|---|---|
| 1 | Correct | The exchange standardizes the contract specifications. |
| 2 | Correct core idea | Settlement-based gains/losses are debited or credited; required margin is a separate concept. |
| 3 | Needs precision | Maintenance is not merely a daytime requirement; see margin definitions above. |
| 4 | Partly correct | Leverage permits exposure larger than equity. An adverse move can create losses beyond deposited funds; large notional alone does not cause a loss. |
| 5 | Correct, with condition | Selling the same quantity of the same expiry offsets the long. A different expiry does not close it. |
| 6 | Needs precision | Notional is price × multiplier × quantity. Planned stop risk includes costs and is not guaranteed by the trigger. |
| 7 | Correct; add change over time | Specifications differ across products and can change. |
| 8 | Correct; add exact status | Verify identity, current registration/membership status, and disciplinary history. An NFA ID alone does not prove current registration. |
| 9 | Needs correction | Fill models, data/latency/queue assumptions, and emotional pressure differ. Simulation may model slippage; it is not universally absent. |
| 10 | Correct response | Stop submitting orders when the mode is uncertain; verify intended simulation mode, account, and existing order/position state. |

For question 8: [NFA BASIC explanation](https://www.nfa.futures.org/investors/investor-resources/files/2023-WIW-Transcript.pdf). For questions 9–10: [Sierra Chart Trade Simulation](https://www.sierrachart.com/index.php?page=doc/TradeSimulation.php).

In Sierra Chart internal simulation, fills depend on the documented bid/ask/last-price rules and replay assumptions. Simulated execution cannot prove the exact fills that a live order would have received. Lack of real financial stakes also changes the experience.

## Coach feedback — points à reformuler toi-même

Tes bonnes bases : rôle de couverture des futures, sens long/short, valeur du tick ES, principe du mark-to-market, capital que tu peux te permettre de perdre et arrêt en cas de doute sur le mode de compte.

À consolider en priorité :

1. **Exchange / clearinghouse :** qui apparie les ordres, qui devient contrepartie centrale ?
2. **Offset / settlement :** fermer une position et régler un contrat à l'échéance sont deux opérations différentes.
3. **Marge / exposition :** le dépôt demandé ne fixe ni la valeur du contrat ni la perte maximale.
4. **Contrat / échéance :** chaque produit a ses mois cotés et ses règles ; ne généralise pas le troisième vendredi.
5. **Simulation :** explique ses hypothèses d'exécution plutôt que d'affirmer qu'elle n'a jamais de slippage.

Relis ces corrections, puis reformule ces cinq distinctions sans copier le texte. Cette version corrigée ne prouve pas encore une maîtrise autonome. Aucun score global ni validation de semaine n'est attribué ici ; le laboratoire plateforme et les autres preuves restent à vérifier séparément.
