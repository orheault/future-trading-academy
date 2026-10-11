# Session Plan — Week 3, MCL Brief 05

**Status:** Student A/B/C price rules accepted; operational rules frozen v1 on 2026-10-07 before actual-release retrieval and post-event prices; mechanism caveats instructor-assisted; observation pending
**Template:** Adapted from templates/SESSION-PLAN.md
**Preparation date:** 2026-10-06 America/Toronto
**Historical date:** 2026-09-16
**Instrument/contract:** MCLV26-NYMEX[M], October 2026, one-minute chart #9 screenshot-verified; selected from reported September 15 volumes
**Session:** New York morning
**Data/account mode:** Historical replay, observation only; screenshot verifies paused 8.00x Single Chart / Standard Replay / Start Paused, September 16 10:25 start, latest chart timestamp 10:24:59
**Chart time zone:** New York explicitly confirmed by student; Continuous Contract=None also explicitly confirmed, settings not shown in screenshot
**Actual study duration:** Unreported
**Historical information cutoff:** September 16 2026 10:29:59 New York
**Freeze timestamp:** 2026-10-07 16:14:34 UTC / 2026-10-07 12:14:34 America/Toronto (clock-verified decision time); snapshot saved before target release retrieval

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

### Student scenarios received and final rules recorded — 2026-10-07

Student submission, verbatim (formatting normalized):

> A:
> 1. Lorsque les stocks augmentent, l'offre s'agrandi, alors les investisseurs peuvent anticiper une diminution du prix par baril.
> 2. J'anticipe que le prix par baril de P5 et P15 sera inférieur à P0
> 3. Si P5 ou P15 est supérieure ou égale à P0, cela invaliderait mon scénario.
>
> B:
> 1. Lorsque les stocks diminuent, l'offre diminue, alors les investisseurs peuvent anticiper une augmentation du prix par baril.
> 2. J'anticipe que le prix par baril de P5 et P15 sera supérieure à P0
> 3. Si P5 ou P15 est inférieure ou égale à P0, cela invaliderait mon scénario.
>
> Aucun:
> 1. Les investisseurs pourrait anticiper une variation nulle comme étant une continuation du current trend.
> 2. J'anticipe que P5 est inférieure à P0 ainsi que P15 supérieure à P0.
> 3. Ce qui invalide le scénario: P5 >= P0 ou P15 <= P0

Assessment: all three price predicates and logical complements are correct, including OR/equality. Accept without another repetitive check. Student supplied a genuine third prediction under the "Aucun" label; preserve it as scenario C at a reported zero stock change, replacing the previously proposed no-scenario-at-zero design before outcome access. This is a user-supplied prospective change, not hindsight fitting.

Instructor mechanism refinement: inventories reflect a balance of inflows/outflows; their increase alone does not establish increased production/supply flow, and a draw alone does not establish reduced supply. Imports, exports and refinery crude inputs can affect the balance. Retain the student's proposed directional pressure as conditional, not causal fact. C's P5 below/P15 above is a checkpoint reversal relative to P0, not a defined continuation of an existing trend; it is a testable price-path hypothesis without an established causal rationale. Do not credit full independent mechanism mastery.

No target September 16 EIA actual or post-event MCL prices retrieved at freeze. Earlier later-week incidental search exposure remains disclosed above and is excluded from the information set. Market expectation remains unknown; zero is a teaching threshold, not consensus.

### Scenario A — final v1
- Condition: published weekly change in commercial crude stocks excluding SPR >0.
- Mechanism: a build could be interpreted as a looser balance and weigh on oil, depending on its drivers and expectations; not proof of higher supply flow.
- Expected evidence: P5 < P0 AND P15 < P0.
- Invalidation: P5 >= P0 OR P15 >= P0.
- Permitted action: observe only.

### Scenario B — final v1
- Condition: published weekly change in commercial crude stocks excluding SPR <0.
- Mechanism: a draw could be interpreted as a tighter balance and support oil, depending on drivers and expectations; not proof of lower supply flow or higher final consumption.
- Expected evidence: P5 > P0 AND P15 > P0.
- Invalidation: P5 <= P0 OR P15 <= P0.
- Permitted action: observe only.

### Scenario C — final v1, student originally labelled "Aucun"
- Condition: published weekly change in commercial crude stocks excluding SPR =0.
- Expected evidence: P5 < P0 AND P15 > P0.
- Invalidation: P5 >= P0 OR P15 <= P0.
- Rationale: student proposes this path; no claim that unchanged inventories imply it or continuation of trend.
- Permitted action: observe only.

### Measurement and missing-data rules — final v1

- Use signed weekly change as stated in the original EIA highlights, in millions of barrels (rounded to one decimal); C refers to zero at that published precision, not proof of exact zero underlying change. Period: week ending September 11, publication September 16 10:30 New York. Expectation remains unknown; do not calculate a consensus surprise.
- T0 10:30; P0 completed 10:29:00–10:29:59 Last/Close; P5 completed 10:34:00–10:34:59, available 10:35; P15 completed 10:44:00–10:44:59, available 10:45. All checkpoint prices unknown at freeze. Units USD/barrel, MCLV26.
- A/B/C partition the valid published changes; missing required release or checkpoint data means not assessable, not zero. Evaluate only the activated scenario. No monotonic path required between checkpoints.
- Original drafts and setup instructions above are preserved history, superseded by these final rules. No risk/order permission changes.

## Risk

- Maximum risk per trade / daily stop: N/A — observation only.
- Maximum trades: 0.

## Post-session audit

Pending actual data, signed comparisons, activation/evaluation, evidence, causal limits and student process lesson. Four of five guided cases remain accepted; this draft supplies no additional completion, score or study duration.
