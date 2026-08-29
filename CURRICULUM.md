# Futures Trading Academy — Curriculum v1.0

**Duration:** 24 nominal weeks  
**Default workload:** 8 hours/week  
**Instruction language:** English  
**Explanation language:** English or French  
**Primary platform:** Sierra Chart  
**Primary instrument:** MES  
**Commodity observation track:** MGC and MCL

## 1. Training objective

At the end of the program, the student should be able to:

1. explain futures contract mechanics, leverage, margin, settlement, expiration, and rollover;
2. calculate tick value, notional exposure, stop risk, position size, and results in R;
3. distinguish fundamental context from a trade trigger;
4. read market structure through trend, balance, imbalance, acceptance, and rejection;
5. use TPO/Market Profile, Volume Profile, DOM, Time & Sales, and Numbers Bars without treating any one display as a prediction machine;
6. specify one setup with objective context, entry, invalidation, target, and exclusion rules;
7. test that setup with a reproducible protocol and separate in-sample from out-of-sample evidence;
8. execute the setup in replay and forward simulation with controlled risk;
9. evaluate process quality independently from P&L; and
10. make a documented live-readiness decision without assuming that course completion implies profitability.

## 2. Student profile and working assumptions

Known:

- Olivier is bilingual and prefers to learn professional terminology in English.
- Olivier has a developer profile that can support structured data analysis and later automation.
- The target is futures and commodities, with Sierra Chart for simulation and possible later execution.
- A USD 10,000 live account has been discussed.

To validate during Week 1:

- prior market and chart-reading experience;
- weekly availability and preferred session times;
- comfort with probability and descriptive statistics;
- actual financial risk capacity, which is different from account size;
- jurisdiction, broker eligibility, taxes, and data-feed constraints;
- whether discretionary execution or later systematic research is the better fit.

Until validated, the program assumes a beginner-to-intermediate starting point and uses conservative risk rules.

## 3. Program rules

### 3.1 Progress is gate-based

A week can be repeated. A phase is not passed merely because four calendar weeks elapsed. Missing evidence, rule violations, or weak comprehension extend the phase.

### 3.2 One market first

MES is the main learning instrument because its Micro sizing supports fine-grained risk control. MGC and MCL are observed to learn commodity-specific fundamentals. They are not added to execution practice until the student demonstrates competence on one instrument.

### 3.3 One setup first

The program develops one setup before considering a second. A setup is a testable decision process, not a chart pattern or an indicator signal.

### 3.4 Process before outcome

A compliant losing trade can be graded A. A profitable rule-breaking trade is graded F. Every result is measured both financially and behaviorally.

### 3.5 No live-trading promise

The final gate produces one of three decisions: `NOT READY`, `READY FOR MORE SIMULATION`, or `ELIGIBLE TO CONSIDER LIMITED LIVE TRADING`. Only the student can make the final financial decision.

## 4. Evaluation system

Each week is scored out of 100:

| Component | Weight |
|---|---:|
| Concept comprehension | 25 |
| Practical lab | 35 |
| Deliverable quality | 20 |
| Journal completeness | 10 |
| Process and risk compliance | 10 |

Weekly pass mark: **80/100**, with no critical safety failure.

Critical safety failures include:

- sending a live order during a simulation-only phase;
- trading the wrong contract month through avoidable negligence;
- taking a trade without a defined invalidation and risk amount;
- disabling or bypassing a loss limit;
- altering historical data or excluding valid losing observations to improve results;
- changing setup rules during locked out-of-sample testing.

## 5. Program overview

| Phase | Weeks | Focus | Phase gate |
|---|---:|---|---|
| I | 1–4 | Futures foundations and platform safety | Contract and operations competency |
| II | 5–8 | Market structure and Auction Market Theory | Context and profile competency |
| III | 9–12 | Order flow and execution evidence | Order-flow interpretation competency |
| IV | 13–16 | Strategy engineering and testing | Edge-evidence gate |
| V | 17–20 | Replay, simulation, and psychology | Simulation-consistency gate |
| VI | 21–24 | Operational and live readiness | Final readiness decision |

---

# Phase I — Futures Foundations

## Week 1 — Risk, ecosystem, and futures purpose

**Outcome:** Explain why futures exist, who uses them, and why leverage creates asymmetric danger for an underprepared retail trader.

**Learn**

- standardized contracts; exchange and clearinghouse roles;
- hedger versus speculator;
- long and short positions;
- leverage, performance bond/margin, and daily mark-to-market;
- cash settlement versus physical delivery;
- CFTC, NFA, FCM, broker, exchange, and data-feed roles;
- why only risk capital may be considered.

**Study:** R01, R02, R03, R04, and Book B01 Introduction/Chapter 1.

**Platform lab:** Install or open Sierra Chart; create a simulation-only chartbook; locate the trade simulation indicator; do not configure live routing.

**Practical lab:** Build a one-page ecosystem map and compare a futures contract with a stock and a forward contract.

**Deliverable:** `exercises/week-01/ASSIGNMENT.md` plus baseline answers in `PROGRESS.md`.

**Pass condition:** 80% on the Week 1 quiz and a correct explanation of why losses can exceed the initial deposit.

## Week 2 — Contract specifications and trade mathematics

**Outcome:** Calculate exposure and risk without relying on a platform P&L display.

**Learn**

- symbol, contract month code, expiration, rollover, and active contract;
- contract multiplier, tick size, tick value, and point value;
- notional value versus margin versus risk-to-stop;
- order quantity, commissions, fees, bid/ask spread, and slippage;
- market, limit, stop, stop-limit, bracket, and OCO orders.

**Study:** R01, R05, R06, R07, R08, and B01 contract mechanics sections.

**Platform lab:** Open MES, locate the contract specification, identify the active month, and create a simulated bracket order without transmitting it.

**Practical lab:** Complete 25 contract-math problems, including long/short P&L, risk-to-stop, and estimated round-trip costs.

**Deliverable:** `notes/contract-math.md` with formulas and worked examples for MES, MNQ, MGC, and MCL using current official specifications.

**Pass condition:** 100% accuracy on safety-critical tick-value and stop-risk calculations; 80% overall.

## Week 3 — Fundamental context for indices, gold, and crude oil

**Outcome:** Build a daily catalyst map without turning macro opinions into unbounded directional bets.

**Learn**

- scheduled versus unscheduled information;
- equity-index drivers: Fed, rates, CPI, employment, earnings, volatility;
- gold drivers: real yields, USD, inflation expectations, central banks, risk sentiment;
- crude drivers: inventories, production, OPEC+, refinery utilization, imports/exports, seasonality, curve structure;
- spot/futures basis, contango, backwardation, and roll considerations;
- expectations versus surprise and the danger of narrative hindsight.

**Study:** R09, R10, R11, R12, and R13.

**Platform lab:** Create an economic-event annotation routine and separate pre-event, event, and post-event observations.

**Practical lab:** Produce five pre-session catalyst briefs: three MES, one MGC, and one MCL. Grade the process after the session without rewriting the original hypothesis.

**Deliverable:** `templates/SESSION-PLAN.md` used five times in `research/`.

**Pass condition:** Each brief distinguishes known facts, expectations, scenarios, and invalidation; no hindsight edits.

## Week 4 — Sierra Chart basics and Foundation Gate

**Outcome:** Operate the platform safely and demonstrate contract competency.

**Learn**

- chartbooks, symbols, sessions, time zones, tick-size settings, and data continuity;
- delayed versus real-time data;
- internal Trade Simulation Mode versus Simulated Futures Trading Service;
- order confirmation, flatten/cancel, Trade Activity Log, backups, and emergency procedures;
- replay limitations and fill-model assumptions.

**Study:** R14, R15, R16, R17, R18, and `SIERRA-CHART-SETUP.md`.

**Platform lab:** Build the four-chartbook structure described in `SIERRA-CHART-SETUP.md`; save a backup copy.

**Practical lab:** Run a 30-minute replay, place bracketed simulated orders, flatten safely, and export/reconcile the activity log.

**Deliverable:** Platform safety checklist plus screenshots stored under `journal/screenshots/week-04/`.

**Foundation Gate**

- 85% closed-book concept exam;
- 100% on ten tick/risk calculations;
- correct rollover and settlement explanation;
- successful simulation emergency drill;
- zero live orders.

If any safety item fails, repeat Week 4.

---

# Phase II — Market Structure and Auction Market Theory

## Week 5 — Price structure and session context

**Outcome:** Describe the market before adding profiles or order-flow tools.

**Learn**

- swing structure, trend, range, impulse, correction, breakout, and failed breakout;
- prior-day high/low, overnight high/low, opening gap, opening range, and ATR;
- regular versus overnight session context;
- volatility regime and location within a multi-day range;
- observation versus inference.

**Study:** R19 and B02 Part I.

**Sierra lab:** Create a clean context chart with price, session markers, prior-day levels, and ATR only.

**Practical lab:** Annotate 20 MES sessions without indicators. Write a pre-open structural hypothesis and a post-close audit for ten of them.

**Deliverable:** 20 observation rows in `Observations` and five annotated screenshots.

**Pass condition:** Context labels are internally consistent and do not use future information.

## Week 6 — Auction Market Theory

**Outcome:** Explain price movement as a continuous auction.

**Learn**

- balance, imbalance, price discovery, and facilitated trade;
- acceptance versus rejection;
- initiative versus responsive activity;
- excess, failed auction, and migration of value;
- timeframe participation as a hypothesis, not a directly observed identity;
- balance → imbalance → new balance.

**Study:** B02 Parts II–III and B03 selected chapters.

**Sierra lab:** Replay ten sessions on a clean chart and pause at predefined times to state the current auction condition.

**Practical lab:** Classify 50 market snapshots as balance, transition, or imbalance and record confidence before seeing the next segment.

**Deliverable:** `notes/auction-market-theory.md` written in your own words.

**Pass condition:** At least 80% consistency on a reviewed classification set and clear separation of evidence from story.

## Week 7 — Volume Profile

**Outcome:** Use volume-at-price to describe where trade was accepted or avoided.

**Learn**

- VPOC, value area, HVN, LVN, distribution shape, and composite profiles;
- developing versus completed profiles;
- session selection and why profile boundaries matter;
- volume acceptance does not imply directional prediction;
- naked levels and the danger of treating them as automatic magnets.

**Study:** R20 and B03 profile sections.

**Sierra lab:** Add Volume by Price to a dedicated chart; verify session times and tick size; compare daily and five-day composites.

**Practical lab:** Profile 20 sessions and document open location, value migration, POC migration, and close location.

**Deliverable:** 20 complete profile observations in the journal.

**Pass condition:** Correctly identify profile elements and explain at least three cases where a level failed to produce a reversal.

## Week 8 — TPO/Market Profile and Profile Gate

**Outcome:** Integrate time-at-price and volume-at-price without conflating them.

**Learn**

- TPO, TPO POC, TPO value area, Initial Balance, range extension, single prints, excess, poor high/low;
- open inside/outside prior value and range;
- normal, normal variation, trend, neutral, and double-distribution descriptions as ex-post structure—not entry signals;
- TPO versus Volume Profile calculations and limitations.

**Study:** R21 and B02 profile chapters.

**Sierra lab:** Build the `PROFILE` chartbook; verify 30-minute subperiods and session definitions.

**Practical lab:** Analyze 20 unseen MES sessions, recording the hypothesis at the open, after the Initial Balance, and at the close.

**Deliverable:** A concise daily profile checklist added to `templates/SESSION-PLAN.md`.

**Profile Gate**

- 85% terminology exam;
- at least 16 of 20 reviewed sessions correctly describe open location and auction condition;
- no more than two hindsight-contaminated observations;
- explain TPO POC versus Volume POC and why they may differ;
- present three failed profile-based predictions and the lesson from each.

---

# Phase III — Order Flow and Execution Evidence

## Week 9 — Orders, DOM, and Time & Sales

**Outcome:** Understand what order-flow tools display and what they cannot prove.

**Learn**

- market versus limit orders; bid, ask, spread, and queue;
- resting liquidity, executed volume, cancellation, and replenishment;
- aggressor classification;
- DOM and Time & Sales reading;
- spoofing risk, hidden liquidity, and the difference between displayed intent and executed fact;
- latency and replay-data limitations.

**Study:** R22, R23, and B04 microstructure chapters.

**Sierra lab:** Build an observation-only Trade DOM and Time & Sales window; record replay-depth availability.

**Practical lab:** Observe ten 15-minute windows at the MES open or another consistently selected period. Record only directly observable events.

**Deliverable:** `notes/order-book-evidence.md` with an evidence hierarchy.

**Pass condition:** Correctly distinguish resting, canceled, and executed liquidity in reviewed examples.

## Week 10 — Numbers Bars, delta, and imbalance

**Outcome:** Read bid/ask execution without assuming delta predicts price.

**Learn**

- bid × ask volume, bar delta, cumulative delta, diagonal imbalance, stacked imbalance;
- unfinished auction and zero prints as platform-defined displays;
- positive delta with falling price and negative delta with rising price;
- why thresholds must be specified and tested;
- data quality, chart settings, and reproducibility.

**Study:** R22 and Sierra Chart Numbers Bars video in R24.

**Sierra lab:** Configure a minimal Numbers Bars chart and save exact settings in `SIERRA-CHART-SETUP.md` notes.

**Practical lab:** Label 100 preselected bars for price direction, delta sign, location, and next-bar outcome. Do not create entry rules yet.

**Deliverable:** Journal observation set plus five delta-divergence counterexamples.

**Pass condition:** Explain why delta is executed aggressor imbalance, not a complete measure of buying or selling pressure.

## Week 11 — Absorption, exhaustion, and initiative

**Outcome:** Form falsifiable hypotheses about order-flow behavior at meaningful locations.

**Learn**

- operational definitions of absorption and exhaustion;
- continuation versus failure after aggressive volume;

- price response relative to volume, delta, and location;
- initiative versus responsive behavior;
- confirmation bias and label leakage.

**Study:** B04 selected chapters and Week 9–10 evidence.

**Sierra lab:** Replay 30 candidate sequences at prior value edges, overnight extremes, and profile LVNs.

**Practical lab:** Before revealing the next segment, label `absorption candidate`, `exhaustion candidate`, `initiative continuation`, or `insufficient evidence` and assign confidence.

**Deliverable:** 30 blinded sequences in `Observations` with screenshot references.

**Pass condition:** At least 80% process compliance; `insufficient evidence` is used when criteria are absent.

## Week 12 — Context + profile + order flow integration

**Outcome:** Use order flow as execution evidence inside a prior contextual hypothesis.

**Learn**

- top-down decision chain: regime → location → scenario → trigger → invalidation;
- signal stacking versus double-counting correlated evidence;
- when not to trade;
- order-flow confirmation latency and adverse selection;
- difference between analysis confidence and permitted risk.

**Study:** Review Weeks 5–11 and B05 playbook chapters.

**Sierra lab:** Use `CONTEXT`, `PROFILE`, and `ORDER-FLOW` chartbooks in synchronized replay.

**Practical lab:** Complete 20 decision cases with a forced choice among long, short, or no trade. `No trade` must remain a normal outcome.

**Deliverable:** First draft decision tree in `PLAYBOOK.md`, still marked `RESEARCH ONLY`.

**Order-Flow Gate**

- 85% concept exam;
- 24 of 30 blinded labels follow the operational definitions;
- 20 decision cases contain predeclared invalidation;
- no live trading and no rule changes made after outcome reveal;
- verbally explain at least five limitations of DOM/footprint evidence.

---

# Phase IV — Strategy Engineering and Testing

## Week 13 — From idea to setup specification

**Outcome:** Convert one contextual hypothesis into testable rules.

**Learn**

- universe, session, context, location, trigger, entry, stop, target, management, and exclusions;
- primary outcome and secondary diagnostics;
- ambiguous cases and decision priority;
- costs and slippage assumptions;
- versioning and rule freeze.

**Study:** B05, B06 selected chapters, and `templates/SETUP-SPEC.md`.

**Practical lab:** Draft Setup 001, preferably a failed-auction/return-to-value hypothesis if evidence supports it. Create ten positive and ten negative examples.

**Deliverable:** Setup 001 v0.1 in `PLAYBOOK.md` with every required field completed.

**Pass condition:** Another person could label an occurrence from the written rules without asking what the author “meant.”

## Week 14 — Manual backtest protocol and data integrity

**Outcome:** Collect observations reproducibly without selecting only attractive charts.

**Learn**

- sampling frame, inclusion/exclusion, consecutive-session sampling;
- in-sample versus out-of-sample;
- look-ahead bias, survivorship bias, selection bias, and data snooping;
- MAE, MFE, R multiple, missed trades, and rule deviations;
- sample-size uncertainty and why 20 trades prove little.

**Study:** B06 research chapters and CFTC system-testing warning R25.

**Practical lab:** Lock Setup 001 v0.2 and collect the first 50 consecutive-session observations, including valid no-trade sessions.

**Deliverable:** Complete `Backtest` rows with screenshot evidence and a documented sampling protocol.

**Pass condition:** No retroactive exclusions; fewer than 5% unresolved classification cases.

## Week 15 — Expectancy, risk, and robustness

**Outcome:** Evaluate the distribution, not just win rate or total P&L.

**Learn**

- R multiple, expectancy, win rate, average win/loss, profit factor;
- drawdown, losing streaks, dispersion, MAE/MFE, and time in trade;
- gross versus net results;
- risk of ruin intuition and dependence between trades;
- regime segmentation without p-hacking.

**Study:** B07 probability/statistics selections and `RISK-MANAGEMENT.md`.

**Practical lab:** Extend to at least 100 in-sample observations. Analyze results overall and by predeclared regime, session segment, and entry quality.

**Deliverable:** Setup 001 research memo: hypothesis, method, sample, results, limitations, and decision.

**Pass condition:** Results reconcile to the journal; costs are included; weaknesses are reported as prominently as strengths.

## Week 16 — Out-of-sample test and Edge-Evidence Gate

**Outcome:** Test locked rules on unseen data.

**Learn**

- rule freeze and test registration;
- out-of-sample evaluation;
- sensitivity to entry, stop, costs, and one-tick slippage;
- reject, revise-and-retest, or advance decisions;
- practical versus statistical significance.

**Practical lab:** Freeze Setup 001 v1.0 before revealing the test period. Collect at least 30 valid out-of-sample occurrences from consecutive eligible sessions.

**Deliverable:** Out-of-sample report and decision recorded in `PLAYBOOK.md` and `CHANGELOG.md`.

**Edge-Evidence Gate**

- at least 100 valid in-sample and 30 valid out-of-sample occurrences;
- locked rules during out-of-sample testing;
- positive net expectancy in the combined sample after conservative costs;
- no single trade contributes more than 20% of total net R;
- profit factor above 1.10 in the combined sample;
- documented performance under one-tick-worse entry or equivalent slippage stress;
- all exclusions justified by predeclared rules.

These are minimum screening criteria, not proof of a permanent edge. If the setup fails, return to Week 13 with a new version and a new untouched test set.

---

# Phase V — Replay, Forward Simulation, and Psychology

## Week 17 — Deliberate replay practice

**Outcome:** Execute the locked setup without pausing to invent rules.

**Learn**

- replay fidelity and limitations;
- deliberate practice versus entertainment;
- decision latency, order entry, bracket use, and cancellation;
- pre-trade verbalization and post-trade tagging;
- clean separation of planned and unplanned trades.

**Study:** R15, R16, R17, and B08 deliberate-practice chapters.

**Practical lab:** Ten full-session replays at realistic speed; use the provisional risk plan and hide future bars.

**Deliverable:** Minimum 20 qualified replay trades or ten documented no-trade sessions.

**Pass condition:** 90% setup adherence and 100% hard-risk compliance.

## Week 18 — Forward paper trading

**Outcome:** Execute in an unfolding market using the Sierra Chart Simulated Futures Trading Service or equivalent safe simulation.

**Learn**

- server-based simulation versus chart replay;
- daily plan, event risk, order audit, and end-of-day reconciliation;
- missed trade versus bad trade;
- no-trade days and opportunity scarcity;
- operational errors as a separate category.

**Study:** R16, R18, and `RISK-MANAGEMENT.md`.

**Practical lab:** Five to ten live-market simulation sessions using delayed or real-time data as appropriate. Use only Setup 001.

**Deliverable:** Every decision logged; broker/platform P&L reconciled to the journal.

**Pass condition:** Zero hard-limit breaches and at least 90% complete trade records.

## Week 19 — Trading psychology as execution engineering

**Outcome:** Identify and interrupt behaviors that degrade rule execution.

**Learn**

- FOMO, revenge trading, overtrading, hesitation, premature exits, stop movement, and P&L fixation;
- trigger → behavior → consequence loops;
- implementation intentions and precommitment;
- outcome bias and process grading;
- physiological state, sleep, and attention as execution inputs.

**Study:** B08 and B09 selected exercises.

**Practical lab:** Tag every impulse and rule deviation; create one if/then intervention for each recurrent error.

**Deliverable:** Personal error playbook and a 5-minute pre-session readiness check.

**Pass condition:** At least 90% process score and every deviation has a documented trigger and correction.

## Week 20 — Simulation Consistency Gate

**Outcome:** Demonstrate stable execution over a meaningful forward sample.

**Practical lab:** Continue until the minimum sample exists: at least 30 forward-simulation sessions and 60 qualified trades. This phase will often extend beyond four calendar weeks.

**Deliverable:** Simulation report with equity curve in R, drawdown, expectancy, costs, setup compliance, time-of-day analysis, and error analysis.

**Simulation Gate**

- 60 qualified forward-simulation trades across at least 30 sessions;
- 100% compliance with hard risk limits;
- at least 95% setup-rule compliance over the final 30 trades;
- positive net expectancy after costs over the full sample and final 30 trades;
- profit factor above 1.10;
- maximum drawdown no worse than the predefined limit;
- no revenge trade, added loser, widened stop, or off-plan setup in the final 20 sessions;
- journal completeness above 95%.

Failure does not imply personal failure. It identifies the module to revisit.

---

# Phase VI — Operational and Live Readiness

## Week 21 — Broker, regulation, costs, and operations

**Outcome:** Understand the account, counterparty, and operational environment before funding.

**Learn**

- FCM and introducing broker roles;
- NFA BASIC and registration/disciplinary checks;
- commissions, exchange fees, routing, market data, margins, and liquidation policy;
- segregated customer funds and what protections do and do not mean;
- account agreements, risk disclosure, permissions, and tax-record needs;
- platform outage, internet outage, stuck order, and emergency contact process.

**Study:** R03, R04, R26, and broker primary documents when a broker is shortlisted.

**Practical lab:** Compare at least two eligible brokers using a written checklist. Do not select on intraday margin alone.

**Deliverable:** Broker due-diligence memo and complete emergency procedure.

**Pass condition:** NFA/CFTC registration verified where applicable; all costs and liquidation rules documented from primary sources.

## Week 22 — One-Micro live-readiness design

**Outcome:** Translate the validated setup into a conservative, executable one-Micro plan.

**Learn**

- risk-to-stop under a one-contract minimum;
- skip-trade rule when one Micro exceeds the risk budget;
- daily, weekly, and drawdown stops;
- scheduled-event restrictions;
- differences between simulation and live fills/behavior;
- no scaling until a separate post-live gate.

**Study:** `RISK-MANAGEMENT.md` and the selected broker's current rules.

**Practical lab:** Run ten stress scenarios: gap through stop, platform loss, rejected order, partial fill, wrong quantity, wrong contract month, news spike, daily-limit hit, repeated losses, and unexpected open position.

**Deliverable:** Signed live-readiness checklist. This is still a simulation exercise.

**Pass condition:** Every scenario has a specific action and emergency contact path.

## Week 23 — Final forward validation and adversarial review

**Outcome:** Try to falsify readiness rather than defend it.

**Learn**

- robustness across volatility and session conditions;
- concentration risk and best-day dependence;
- strategy decay and monitoring triggers;
- behavioral relapse indicators;
- capital-preservation decision rules.

**Practical lab:** Continue simulation for at least ten additional sessions. Re-run results with higher costs/slippage and remove the best trade and best day.

**Deliverable:** Red-team report listing every reason the strategy or trader may not be ready.

**Pass condition:** The plan remains acceptable under the predeclared stress tests, or the decision is explicitly deferred.

## Week 24 — Final assessment and readiness decision

**Outcome:** Produce an evidence-based decision and a 90-day next-step plan.

**Final portfolio**

- completed concept examinations;
- platform safety evidence;
- validated Setup 001 specification;
- in-sample, out-of-sample, replay, and forward-simulation reports;
- risk plan and emergency procedures;
- broker due diligence;
- psychology/error playbook;
- complete journal and progress log.

**Final Gate**

- all prior phase gates passed;
- at least 150 total historical setup occurrences, including at least 30 out-of-sample;
- at least 60 forward-simulation trades across 30 sessions;
- positive net expectancy after conservative costs in historical and forward samples;
- 95% or better setup compliance and 100% hard-risk compliance in the final 30 trades;
- no unresolved critical operational issue;
- risk capital and personal financial suitability reassessed independently of the USD 10,000 account target;
- written acceptance that live results can differ materially from simulation.

**Decision options**

1. `NOT READY` — return to the identified module.
2. `READY FOR MORE SIMULATION` — evidence is promising but incomplete.
3. `ELIGIBLE TO CONSIDER LIMITED LIVE TRADING` — consider one Micro under the provisional risk plan, subject to personal suitability, broker approval, and an explicit separate decision.

## 6. Post-curriculum scaling gate

Contract quantity may not increase merely because the account grew or a winning streak occurred. Earliest review:

- minimum eight weeks of live execution;
- minimum 60 live trades;
- positive expectancy after all costs;
- at least 95% setup compliance and 100% hard-risk compliance;
- maximum drawdown within plan;
- no unresolved operational or behavioral issue;
- projected risk remains within the current percentage and dollar limits.

If any condition fails, remain at one Micro or return to simulation.

