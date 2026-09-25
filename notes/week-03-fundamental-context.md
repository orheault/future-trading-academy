# Week 3 — Fundamental Context

**Instructor reference — not student evidence**  
**Prepared:** 2026-09-24  
**Mode:** observation only; MES primary, MGC/MCL comparison  
**Goal:** Build a catalyst map with facts, expectations, conditional scenarios and explicit invalidation.

## 1. Information is not an entry trigger

A catalyst is information that may change expectations and market prices. Scheduled catalysts include inflation releases, employment reports and central-bank decisions. Unscheduled catalysts include unexpected policy announcements, geopolitical developments and production disruptions.

Separate these layers:

| Layer | Meaning | Example — fictional |
|---|---|---|
| Fact | Verifiable information, with source and timestamp | Core CPI month over month was released at +0.4% |
| Expectation | A forecast available before the release | A named survey's median forecast was +0.2% |
| Hypothesis | A conditional explanation to test | The upside inflation surprise may raise expected rates and pressure equities |
| Observation | What the selected data actually show | MES closed below its pre-release reference at T+5 minutes |
| Opinion | A personal judgment without an operational test | Equities are too expensive |

A survey median is evidence about a surveyed group's forecasts, not a complete measurement of everything priced into a market. Record the provider and publication time. If a historical forecast cannot be verified, write `unknown`; never invent it from the subsequent price reaction.

## 2. Previous, expected and actual are different comparisons

Fictional example, using the SAME indicator, period and seasonal-adjustment basis:

- Previous core CPI month-over-month reading: +0.3%.
- Pre-release consensus: +0.2%.
- Actual release: +0.4%.
- Actual minus consensus: +0.2 percentage points, or 20 basis points.
- Actual minus previous: +0.1 percentage point.

The first difference describes a surprise relative to the chosen forecast; the second describes a change from the prior reading. Do not label either as a percentage change. Distinguish headline from core, monthly from annual, and original from revised values. A release can contain conflicting components.

## 3. MES: two channels can compete

Equity values depend partly on expected company cash flows and the rates used to value them. Strong employment may improve the earnings outlook while also encouraging expectations of tighter monetary policy. Inflation surprises can change expected rates, but do not determine the next price move mechanically. Earnings, guidance, positioning and uncertainty can also matter.

For a brief, write a conditional chain: `If the release changes rate expectations in direction X, I will observe whether MES responds in direction Y.` Label the chain as a hypothesis. If rate data are unavailable, do not claim to have verified that channel. Price movement after a release alone does not establish causation.

Source: [Federal Reserve — monetary-policy transmission](https://www.federalreserve.gov/monetarypolicy/monetary-policy-what-are-its-goals-how-does-it-work.htm). Use the [FOMC calendar](https://www.federalreserve.gov/monetarypolicy/fomccalendars.htm) and [BLS calendar](https://www.bls.gov/schedule/) for release dates; verify the exact release time and time zone separately for the selected event.

## 4. MGC: gold and competing drivers

Real yields, the dollar, inflation expectations, central-bank demand and risk sentiment are useful context variables. A forward-looking real yield can be approximated as a nominal yield minus expected inflation over a comparable horizon. Subtracting the latest monthly CPI from a ten-year nominal yield is not an appropriate match.

Higher real yields can increase the opportunity cost of holding non-interest-bearing gold. Dollar strength may weigh on dollar-priced gold, but these are conditional relationships. Counterexample to a mechanical rule: gold and real yields can rise together when other demand or risk factors dominate. Do not infer central-bank buying from an intraday candle.

Sources: [CME — gold and the dollar](https://www.cmegroup.com/openmarkets/metals/2025/Gold-and-the-US-Dollar-An-Evolving-Relationship.html), [CME — real yields and gold](https://www.cmegroup.com/articles/2024/through-the-lens-of-gold.html), [World Gold Council — competing drivers](https://www.gold.org/goldhub/gold-focus/2025/06/you-asked-we-answered-are-fiscal-concerns-driving-gold).

## 5. MCL: inspect the petroleum balance

For an EIA release, distinguish crude inventories from gasoline and distillate inventories. Review production, imports/exports and refinery activity instead of attributing every stock change to end demand. OPEC+ decisions, outages and seasonality provide additional context; distinguish announced policy from observed implementation.

A crude inventory draw means measured stocks fell over the reporting period. It does not, by itself, prove stronger consumption or imply an immediate price rise. A larger expected draw can make an actual draw a comparatively weaker result.

Source and report tables: [EIA — Weekly Petroleum Status Report](https://www.eia.gov/petroleum/supply/weekly/). Check the selected release's schedule, including holiday changes. Course background: [CME — Introduction to Energy](https://www.cmegroup.com/education/courses/introduction-to-energy).

## 6. Basis and the futures curve

State your sign convention: in these notes, `basis = spot price − futures price`. Match commodity, quality, location, units and timestamp before interpreting it.

Across expiries observed at the SAME time:

- Contango: deferred contracts are more expensive than nearby contracts.
- Backwardation: deferred contracts are cheaper than nearby contracts.
- Curves can be mixed; identify the specific expiries being compared.

Fictional oil example: nearby $70/barrel and deferred $72/barrel describe contango between those contracts. They are not a forecast that the nearby contract will rise by $2. Carry costs, storage and the benefit of having physical supply available can influence the curve.

Rolling closes one expiry and opens another. The price difference is not automatically an immediate cash loss of that size on a futures roll. Costs and subsequent price changes matter. Do not treat a continuous-chart rollover gap as a tradable market move without checking the underlying contracts and adjustment method.

Source: [CME — contango and backwardation](https://www.cmegroup.com/education/courses/introduction-to-base-metals/what-is-contango-and-backwardation).

## 7. A testable observation scenario

Instructor-designed exercise rule, not a validated trading setup:

1. Before the event, define P0 as the last completed one-minute candle close before the scheduled release.
2. Fix checkpoints at T+1, T+5 and T+15 minutes and define them consistently as completed candle closes.
3. Hypothesis: an upside inflation surprise may be followed by a price decline that persists through T+15.
4. Observation criterion: T+5 and T+15 closes are both below P0.
5. Invalidation of this precise scenario: either of those closes is at or above P0. Missing data mean `not assessable`, not success or failure.
6. Record the initial response and reversal separately. A higher-than-expected release followed by a rally is valid evidence against this scenario.

These arbitrary checkpoints make the lesson reproducible. One matching episode does not validate an edge or explain causality. No order is part of this exercise.

## 8. Evidence discipline

Freeze the original brief before revealing the event. Add a separately timestamped audit afterward. For replay, record both the real study date and the historical information cutoff. A modern article describing a historical reaction is not pre-event evidence. If you already know the outcome, label the case as a retrospective demonstration and use a fresh case for assessment.

## Student notes — to complete in your own words

- Definition of a catalyst:
- Directly observable evidence:
- One conditional interpretation:
- One limitation:
- One counterexample:
- Sources and timestamps:

