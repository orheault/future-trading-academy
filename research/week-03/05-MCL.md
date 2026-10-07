# Session Plan — Week 3, MCL Brief 05

**Status:** Expiry-price comparison recheck accepted 2026-10-06; prior EIA release verified; expectation unverified, zero-change pedagogical threshold proposed; student scenarios pending, not frozen
**Template:** Adapted from templates/SESSION-PLAN.md
**Preparation date:** 2026-10-06 America/Toronto
**Historical date:** 2026-09-16
**Instrument/contract:** MCLV26-NYMEX[M], October 2026, one-minute chart #9 screenshot-verified; selected from reported September 15 volumes
**Session:** New York morning
**Data/account mode:** Historical replay, observation only; screenshot verifies paused 8.00x Single Chart / Standard Replay / Start Paused, September 16 10:25 start, latest chart timestamp 10:24:59
**Chart time zone:** New York explicitly confirmed by student; Continuous Contract=None also explicitly confirmed, settings not shown in screenshot
**Actual study duration:** Unreported
**Historical information cutoff:** Proposed September 16 10:29:59 New York
**Freeze timestamp:** Pending

## Readiness and information exposure

Student answers "Non" to knowing the September 16 EIA inventory figures or subsequent oil reaction. Record as self-report. Date chosen by event type before outcome access. The same day's later 14:00 FOMC decision is already known from case 4; keep that future event information out of this morning's hypotheses. No September 16 EIA actual or MCL reaction retrieved. Sleep/energy/focus unreported. No orders permitted.

## Known information

- [EIA Weekly Petroleum Status Report schedule](https://www.eia.gov/petroleum/supply/weekly/schedule.php), checked October 6: standard Wednesdays at 10:30 Eastern, no September 16 exception; preceding holiday week released September 10. Proposed event is September 16 10:30 New York.
- [CME Micro WTI product page](https://www.cmegroup.com/markets/energy/crude-oil/micro-wti-crude-oil.contractSpecs.html), checked October 6, identifies MCL. Contract candidates for comparison: MCLV26 (October 2026), MCLX26 (November 2026). Preserve actual Sierra service suffix from Find Symbol rather than guessing it.
- Student reports September 15 volumes MCLV26 195,360 versus MCLX26 37,586; October selected. Values reported, not independently verified; approximately 5.2 times more volume (instructor calculation).
- Proposed study measure: weekly change in US commercial crude inventories excluding the Strategic Petroleum Reserve, in millions of barrels; exact previous/expected/actual vintage and report coverage to verify before freeze. Other report components are context, not substitutes for this measure.
- Previous release: September 10, week ending September 4; commercial crude excluding SPR decreased 0.4 million barrels to 424.1 million (rounded EIA highlights). Expectation for September 16: unverified/unknown; do not invent consensus. Actual: intentionally unretrieved.
- Technical profile/value/regime: not assessed this week.

## Grouped setup task

1. Report September 15 total daily volumes for MCLV26 and MCLX26; justify choosing the higher-volume candidate. Missing data are unknown, not zero.
2. Open selected individual contract as a one-minute chart, New York time, Continuous Contract=None.
3. Set Single Chart / Standard Replay, September 16 10:25:00, Start Paused; send one setup screenshot and confirm settings.
4. Keep replay before 10:30 until information, student scenarios, complete invalidations and final saved rules are ready. Do not collect post-event prices yet.

Proposed later completed-bar measurements: 10:29 P0, 10:34 P5, 10:44 P15. Not frozen yet. Separate expiry-price comparison recheck remains outstanding; volume comparison alone does not satisfy it.

## Scenarios

### Volume choice and replay setup accepted — 2026-10-06

Student submission, verbatim:

> MCLV26: 195360
> MCLX26: 37586
> Je choisi MCLV26 du au plus grand volume que l'autre contrat. Les reglages sont à New York et None.

Accept contract choice among the compared candidates. Saved [September 16 MCL setup](../../journal/screenshots/week-03/2026-10-06_MCLV26_2026-09-16_replay-paused-1025.png). Title identifies MCLV26-NYMEX[M], October 2026, 1 Min #9. Replay paused with correct September 16 10:25 start, Single Chart / Standard Replay / Start Paused checked. Latest time 10:24:59; selected 10:24 bar Open 103.20, High 103.21, Low 103.12, Last 103.19, Volume 115. This completed-bar price is verified but is not event P0 (planned completed 10:29 bar). New York and None are explicit self-report, not visual verification.

Use remaining expiry-price comparison recheck while still before the event: request MCLX26 one-minute replay paused at the same September 16 10:25 New York, and Last from its completed 10:24 bar with screenshot. Compare this to MCLV26 103.19 USD/barrel, same bar interval and measure. Calculate deferred-minus-nearby (November minus October) and classify the relationship between these two expiries as contango, backwardation or equal. Do not label it a spot-futures basis or whole-curve classification. These last-trade bar closes share the minute interval but are not guaranteed synchronous executable quotes; missing/no-trade bar data must be identified rather than invented. Classification pending November data, no mastery inferred.

Keep selected MCLV26 paused before 10:30. No actual EIA outcome or post-event prices retrieved; prior report, expectation and scenarios still pending. Four of five cases accepted, no score/study duration inferred.

### Expiry-price recheck accepted and inventory context prepared — 2026-10-06

Student submission, verbatim:

> 1. 98.29$
> 2. 98.29 - 103.19= -4.9
> 3. Je classifie à backwardation étant donnée que le prix d'octobre est plus élevé.

Correct reading, signed subtraction and relative-expiry classification. Saved [November 10:24 verification](../../journal/screenshots/week-03/2026-10-06_MCLX26_2026-09-16_expiry-comparison-1024.png). MCLX26-NYMEX[M] 1 Min #10, September 16 10:24 completed bar: Open 98.35, High 98.35, Low 98.26, Last 98.29, Volume 64; replay paused at 10:25 with latest time 10:24:59. Paired with verified October Last 103.19 for the same minute, November-minus-October = -4.90 USD/barrel. Backwardation applies between these two expiries; no guaranteed future spot price or executable spread claimed. Accept outstanding expiry-price comparison after earlier remediation; no further repetition needed.

Official previous report located through [EIA archive page](https://www.eia.gov/petroleum/supply/weekly/archive/2026/2026_09_10/wpsr_2026_09_10.php), release September 10 at 12:00 Eastern under holiday schedule, covering week ending September 4. [Original highlights](https://www.eia.gov/petroleum/supply/weekly/archive/2026/2026_09_10/pdf/highlights.pdf) report commercial crude excluding SPR down 0.4 million barrels to 424.1 million; use these rounded figures and distinguish weekly change from stock level. Target September 16 report covers week ending September 11, per archive calendar.

Information audit: targeted previous-report search also returned later EIA landing-page metadata and unrelated later-week stock data; these are excluded from the historical information set. No September 16 actual inventory change or MCL post-announcement prices seen. Do not claim all retrieval results were strictly pre-event. Forecast for September 16 remains unverified; this is not a claim that no forecast exists.

Instructor proposes an explicitly different observation design for this final case: no invented consensus; expected field stays unknown. Use zero weekly inventory change as a transparent pedagogical threshold, not a forecast. A: actual change >0 (stock build); B: actual change <0 (stock draw); exactly 0 neither. This tests price response to builds/draws, not a surprise versus expectations. A draw can still disappoint market expectations; none are verified here. Student should propose mechanism, both P5/P15 inequalities and complete invalidation for each condition before freezing. No directional prediction supplied at this stage. Return to selected MCLV26 replay paused 10:25; proposed checkpoints remain 10:29/10:34/10:44. Four of five cases accepted; no score/duration inferred.

### Scenario A
- Condition, mechanism, expected evidence and invalidation: pending student draft after benchmark research.
- Permitted action: observe only.

### Scenario B
- Condition, mechanism, expected evidence and invalidation: pending student draft after benchmark research.
- Permitted action: observe only.

Neither-scenario and missing-data rules: pending finalization before outcome access.

## Risk

- Maximum risk per trade / daily stop: N/A — observation only.
- Maximum trades: 0.

## Post-session audit

Pending actual data, signed comparisons, activation/evaluation, evidence, causal limits and student process lesson. Four of five guided cases remain accepted; this draft supplies no additional completion, score or study duration.
