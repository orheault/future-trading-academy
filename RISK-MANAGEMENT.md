# Risk Management Policy v1.0

**Applies to:** replay, forward simulation, and any separately authorized future live trading  
**Default account reference:** USD 10,000  
**Status:** Provisional; to be validated during the curriculum

## 1. First principle

The purpose of risk management is not to make a trade safe. It is to keep one error, one trade, one day, or one unstable period from becoming financially or behaviorally catastrophic.

Futures are leveraged. Margin is not the amount at risk. A trader can lose the entire deposit and may owe more. Only genuine risk capital may be considered.

## 2. Definitions

- **1R:** the planned loss if the initial stop is executed, including a conservative allowance for commissions and slippage.
- **Risk-to-stop:** `stop distance in ticks × tick value × contracts + estimated costs/slippage`.
- **Hard limit:** a limit that cannot be overridden during the session.
- **Process violation:** any action outside the current setup or risk policy, regardless of P&L.

## 3. Position-size formula

```text
maximum risk dollars = account reference × risk percentage
risk per contract = stop ticks × tick value + estimated round-trip costs and slippage
contracts = floor(maximum risk dollars ÷ risk per contract)
```

If the result is below one contract, the trade is skipped. The stop is never tightened merely to force a trade into the budget.

## 4. Curriculum simulation limits

Use the same discipline in replay and simulation that would apply live.

| Limit | Rule |
|---|---|
| Contracts | 1 Micro |
| Planned risk per trade | USD 25 maximum (0.25% of the USD 10,000 reference account) |
| Daily stop | -2R or two consecutive losses, whichever comes first |
| Weekly stop | -5R |
| Maximum new trades per day | 3 qualified Setup 001 trades |
| Adding to losers | Prohibited |
| Widening stops | Prohibited |
| Unplanned setup | Prohibited |
| Overnight holding | Prohibited unless a later setup explicitly requires and tests it |

These limits are intentionally conservative. They are training controls, not claims that USD 25 is optimal for every setup or market.

## 5. Provisional future live limits

These rules do not activate automatically. They apply only after the Final Gate and a separate live decision.

| Limit | Initial live rule |
|---|---|
| Quantity | 1 Micro only |
| Risk per trade | Lesser of USD 25 or 0.25% of current account equity |
| Daily stop | -2R, then platform lockout |
| Weekly stop | -5R, then return to simulation and review |
| Strategy drawdown stop | -7.5R from equity peak, then suspend live trading |
| Max trades per day | 3 qualified trades |
| Scaling | Not before the separate post-live scaling gate |

## 6. Pre-trade checklist

A trade is allowed only if every answer is `YES`:

1. Is this the correct symbol and active contract month?
2. Is the platform connected to the intended simulation/live account?
3. Is Setup 001 active and fully qualified?
4. Are context, location, trigger, invalidation, and target documented?
5. Is the initial stop defined from market structure rather than desired dollars?
6. Does one Micro fit within the risk budget?
7. Are scheduled-event restrictions satisfied?
8. Is the daily/weekly loss limit still available?
9. Is the bracket/OCO configuration correct?
10. Is physical and mental readiness acceptable?

One `NO` means no trade.

## 7. Event-risk rules

During training, do not initiate a trade from two minutes before until five minutes after a scheduled Tier-1 U.S. release relevant to the instrument. For MCL, do not trade the first ten minutes around the weekly EIA petroleum-status release. Longer exclusions may be used when volatility or liquidity is abnormal.

These are conservative training constraints and must later be tested against the exact setup. Unscheduled news can still create gap and slippage risk.

## 8. Stop and target rules

- Every order must have a predefined invalidation.
- A protective stop is entered with or immediately after the entry according to the tested bracket workflow.
- A stop may be tightened only if the active playbook version defines the rule.
- A stop may never be widened.
- Profit-taking and trailing logic must follow the active setup version.
- Manual exits are tagged with a reason; discretionary fear is not a valid rule.

## 9. Daily shutdown sequence

Trading stops immediately after:

- the daily loss limit;
- two consecutive losses;
- one hard-rule violation;
- a platform/account mismatch;
- a loss of data integrity;
- an unexpected open position that cannot be reconciled; or
- an emotional-state score below the permitted threshold.

Then:

1. cancel all working orders;
2. confirm position quantity with the authoritative account view;
3. flatten only if a position remains;
4. save the Trade Activity Log;
5. record the event and screenshot;
6. stop for the session—no attempt to recover losses.

## 10. Operational emergency procedure

Before any live consideration, document:

- broker trade-desk phone number;
- account identifier stored securely outside this project;
- backup internet method;
- platform reconnect procedure;
- order-status verification process;
- flatten/cancel-all procedure;
- handling for rejected, duplicate, partial, or stuck orders;
- daily broker liquidation and margin policy.

Never place credentials, recovery codes, or full account numbers in this project.

## 11. Review metrics

Track at minimum:

- net R and net P&L after costs;
- expectancy;
- win rate, average win, and average loss;
- profit factor;
- maximum drawdown and longest losing streak;
- MAE and MFE;
- setup compliance;
- hard-risk compliance;
- error cost in R;
- performance by regime and time segment.

## 12. Scaling rule

Increasing quantity requires all of the following:

- at least eight weeks and 60 live trades at the current size;
- positive expectancy after all costs;
- 95% or better setup compliance;
- 100% hard-risk compliance;
- drawdown within plan;
- no unresolved behavior or operational issue;
- unchanged percentage and dollar-risk logic after quantity increases.

Scaling is reversed after a drawdown or compliance breakdown.

