# Trading Playbook

**Version:** 0.1  
**Status:** RESEARCH ONLY  
**Active live setups:** None

## Admission rule

A setup may become `SIMULATION ACTIVE` only after the Edge-Evidence Gate. It may become `LIVE ELIGIBLE` only after the Final Gate and a separate live-trading decision.

## Setup status vocabulary

- `IDEA`: conceptual possibility; not testable yet.
- `RESEARCH ONLY`: objective draft under historical study.
- `LOCKED OOS`: rules frozen for out-of-sample test.
- `SIMULATION ACTIVE`: passed minimum historical evidence and may be forward tested.
- `SUSPENDED`: evidence or compliance deteriorated.
- `LIVE ELIGIBLE`: completed every gate; still not automatic authorization.

## Decision chain

```text
Regime → Location → Scenario → Trigger → Invalidation → Size → Management → Review
```

If any required link is missing, the decision is `NO TRADE`.

## Setup 001 — Failed Auction / Return to Value

**Status:** IDEA / RESEARCH ONLY  
**Instrument:** MES initially  
**Session:** To define  
**Version:** 0.1  
**Owner:** Olivier

### Hypothesis

When price auctions beyond a well-defined balance extreme or prior value boundary, fails to gain acceptance, and returns into the prior accepted area with confirming execution evidence, continuation back toward an internal reference may occur often enough to exceed costs.

This is a hypothesis, not a fact.

### Required context

- A clearly defined reference balance or prior value area.
- A predeclared boundary: balance high/low, VAH/VAL, or another tested extreme.
- The test occurs during the allowed session and outside excluded event windows.
- Volatility and liquidity conditions fall within the eventual tested range.

### Required location

- Price trades beyond the reference boundary by a minimum/maximum amount to be defined from evidence.
- The excursion is visible without using future bars.

### Candidate trigger

To research, not yet trade:

- lack of continuation beyond the boundary;
- return through the boundary;
- acceptance back inside the prior area;
- optional order-flow evidence such as aggressive-volume failure or absorption, defined objectively.

### Entry

Undefined. Candidate choices must be tested separately:

1. first close back inside the reference;
2. retest of the reclaimed boundary;
3. order-flow trigger after re-entry.

### Invalidation

Undefined. Must be structural, observable, and compatible with one-Micro risk.

### Target and management

Undefined. Candidate references include VPOC/TPO POC, midpoint, or opposite value edge. No choice is active until tested.

### Exclusions

To define before testing:

- scheduled Tier-1 event windows;
- wrong or illiquid contract month;
- abnormal spread/data outage;
- insufficient initial reference balance;
- one-Micro risk exceeds the risk budget;
- late entry after the move has already traveled a defined distance.

### Data fields required

- date, contract, session, direction;
- regime and reference boundary;
- open location and value migration;
- excursion beyond boundary;
- trigger timestamp;
- entry, stop, target, costs;
- result in R, MAE, MFE;
- screenshot before and after;
- compliance grade and ambiguity flag.

### Promotion criteria

See Weeks 13–16 in `CURRICULUM.md`. At minimum: 100 in-sample occurrences, 30 locked out-of-sample occurrences, positive net expectancy after conservative costs, profit factor above 1.10, and transparent stress testing.

## Setup change log

| Version | Date | Status | Change | Reason | New untouched test set required? |
|---|---|---|---|---|---|
| 0.1 | 2026-08-23 | Research only | Initial hypothesis shell | Curriculum initialization | Yes |

## Setup suspension triggers

Suspend a setup if:

- rolling performance breaks a predeclared monitoring threshold;
- market structure or contract behavior materially changes;
- rule ambiguity exceeds 5% of cases;
- costs/slippage eliminate net expectancy;
- compliance falls below 90%; or
- the trader changes rules during execution.

