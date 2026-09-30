# Session Plan — Week 3, MES Brief 01

**Status:** Invalidation recheck accepted after coaching; pre-event rules frozen as v1; replay measurements and audit pending
**Template:** Adapted from `templates/SESSION-PLAN.md`  
**Preparation date:** 2026-09-27  
**Historical date:** 2026-09-11; MESU26 selected; screenshot verifies pre-event intraday coverage through 08:24:59, not the entire event window
**Actual study date/time:** Pending student record  
**Instrument/contract:** MESU26-CME (September 2026), one-minute chart #2, verified in screenshot on 2026-09-28. Header includes [M]. Previous chart was MESZ26.
**Session:** New York morning, before and after the CPI release  
**Data mode:** Historical replay, paused; Single Chart, Standard Replay, speed 1.00, Start Paused checked, start 2026-09-11 08:25:00, visible latest data 08:24:59; verified from screenshot
**Account mode:** Observation only  
**Chart time zone:** New York, per student on 2026-09-28; 08:30 Eastern release corresponds to 08:30 chart time; not independently inspected
**Historical information cutoff:** 2026-09-11 08:29:59 America/New_York  
**Brief frozen at (actual timestamp):** 2026-09-30 01:49:35 UTC / 2026-09-29 21:49:35 America/Toronto (clock-verified decision time); v1 after guided remediation, before the formal release reveal and any submitted post-event chart evidence

## Readiness

- Sleep/energy (1–5): Pending.
- Focus (1–5): Pending.
- Emotional state: Pending.
- Allowed to trade under the plan? No; observation only.
- Is the historical outcome already known to the student? No, per student response on 2026-09-28. Preserve this by preparing scenarios before viewing the event response.
- Historical chart coverage around the event: Screenshot now verifies pre-event bars on September 11 through 08:24:59. Post-event coverage and continuity remain unverified.
- Exact contract choice and evidence available for that historical session: MESU26 selected; reported September 10 volume 1,071,765 versus MESZ26 37,408. Prior-session evidence, not a measurement of announcement-time liquidity.
- Continuous-contract setting: None reported for the original MESZ26 chart; keep None on the selected MESU26 exercise chart. Selected chart setting not independently inspected.

### Preparation record — 2026-09-28

Student reply, verbatim: “1. OUi” / “2. Non”, answering data availability and prior knowledge of the reaction respectively. Exact contract symbol was not provided. Next: obtain the complete Sierra chart symbol and configured chart time zone before locating the release. This is preparation evidence, not a completed brief or a verified platform check. No study duration inferred.

Student follow-up, verbatim: “1. MESZ26” / “2. Fuseau horaire configuré à New York”. Chart symbol and time zone now recorded as student reports.

Contract-context check: [CME equity-index roll calendar](https://www.cmegroup.com/trading/equity-index/rolldates.html), consulted 2026-09-28, lists the customary September 2026 U.S. index roll date as September 14 and expiration as September 18. The study date, September 11, precedes that customary roll. This does not prove which contract had higher volume or make December inherently invalid for observation.

Next check: obtain the value of `Chart > Chart Settings > Symbol > Continuous Contract` without changing it. [Sierra Chart documentation](https://www.sierrachart.com/index.php?page=doc/ContinuousFuturesContractCharts.html) explains that continuous charts can join earlier expiries while retaining the current chart symbol. A MESZ26 header alone does not identify the source expiry of September 11 bars. Historical expiry mapping, adjustment method and relevant data coverage must be understood before freezing the price reference. No announcement result or post-event reaction retrieved.

Student follow-up, verbatim: “La valeur est None”. This resolves the reported continuous-contract setting: the chart is configured for the December contract itself, not stitched earlier expiries. It does not establish which expiry was most active before the event or independently verify data continuity.

Next task: compare contract-specific Historical Daily volume for the completed trade date 2026-09-10 on MESU26 and MESZ26, using non-continuous charts and comparable coverage. This is information available before the September 11 announcement; do not inspect September 11's full-day candle or volume to make the pre-event selection. Week 2 recorded `Download Total Volume for All Contracts for Futures Daily Data = No`; retain that contract-specific setting for this comparison. Record the two observed volumes, not open interest. If the historical expiry/data are unavailable, report that limitation rather than inventing a zero. Prior-session volume informs selection; it does not prove event-time liquidity. Volumes and final selection remain pending.

Student volume submission, verbatim: “MESU26: 1071765” / “MESZ26: 37408” / “Je conclus que je dois prendre le contrat avec échéance de septembre”. These values answer the request for September 10 Historical Daily volume. Date, chart type and volume provenance are carried from the requested task context, not independently verified from a screenshot.

Coach assessment: accept the historical contract-selection reasoning. September volume is approximately 28.65 times December volume on the reported prior session. Select MESU26 for this September 11 observation; do not generalize this choice to today's market. This is a comparison of volumes, not the pending comparison of futures prices across expiries.

Next practical step: open the MESU26 intraday chart with one-minute bars, New York time and no continuous stitching; verify coverage includes September 11 before setting a replay start. Begin paused at September 11, 2026 08:25:00 to prepare the brief before the 08:30 release. Use Start Paused and Single Chart; if entering a start date/time, it must lie within loaded historical data. Reference: [Sierra Chart replay documentation](https://www.sierrachart.com/index.php?page=doc/ReplayChart.html), checked 2026-09-28. A pre-event screenshot is requested; replay setup, scenario writing and the actual freeze timestamp remain pending. Keep the intended information cutoff at 08:29:59; no post-event bars or release outcome should be used to prepare scenarios.

Screenshot received and preserved at [pre-event replay evidence](../../journal/screenshots/week-03/2026-09-28_MESU26_2026-09-11_replay-paused-0825.png). Visible: Sierra Chart 2947, SC Data, [Sim], MESU26-CME, 1 Min, chart #2, Paused 1.00X, Single Chart, Standard Replay, requested start 2026-09-11 08:25:00, Start Paused checked, latest displayed data 2026-09-11 08:24:59. The application's September 28 timestamp is distinct from historical replay time. Right-hand displayed price is 7643.50; it is NOT the final pre-announcement reference P0, which will be defined as the close of the 08:29 one-minute bar. No post-release bars are visible. Time zone and Continuous Contract settings are not shown in this screenshot; preserve their existing evidence limits. No order execution, full account state or study duration inferred.

## Known information

- Scheduled event: U.S. CPI for August 2026, scheduled September 11, 2026 at 08:30 Eastern Time.
- Source: [BLS September 2026 release calendar](https://www.bls.gov/schedule/2026/09_sched.htm), checked 2026-09-27. Calendar only; release outcome not retrieved for this draft.
- The calendar also lists Real Earnings at the same time; do not claim the event window isolates one causal influence.
- Selected indicator: Core CPI, month over month, seasonally adjusted (keep headline and annual measures separate).
- Previous reading available before cutoff: July 2026 Core CPI month over month, seasonally adjusted, +0.2%, in the original [BLS release dated August 12, 2026 at 08:30 ET](https://www.bls.gov/news.release/archives/cpi_08122026.htm), checked September 28. This is the prior observation, not the forecast for August.
- Pre-release expectation benchmark: +0.2% month over month for August Core CPI, reported in Matt Weller's [FOREX.com preview dated September 10, 2026](https://www.forex.com/en-uk/news-and-analysis/us-cpi-preview-the-fed-s-0-3pct-rate-hike-trigger-for-core-cpi/). Attribute to that preview; it describes traders'/economists' expectations but does not identify a survey provider, panel or median methodology. Do not label this an independently audited market-wide consensus.
- Expectation source/provider and timestamp: Matt Weller / FOREX.com, displayed date 10/09/2026 on the UK site; exact publication time not shown. This date precedes the historical cutoff. The article's monetary-policy predictions are opinions and are not adopted as facts in this brief.
- Actual release: [Leave blank until the post-event audit.]
- Search log (2026-09-28, instructor): searched for pre-release September CPI previews and Scotiabank previews; inspected the BLS August 12 archive; the Investing.com AMP preview failed to fetch, its normal page loaded, and its Original Post link led to the dated FOREX.com preview above. No identifiable original consensus survey was verified. Generic search snippets included post-release material; exclude it from scenario construction and do not describe the instructor as blinded to all subsequent information. No August actual figure or post-release market reaction is transcribed into this pre-event brief. Student prior-knowledge status remains based on their earlier report.
- Overnight range and structure: Not assessed yet.
- Prior-day range and value: Not assessed this week unless supported by already-learned methods.
- Current multi-day regime: Not assessed this week.
- Volatility context: Pending observation using only pre-cutoff information.

## Scenarios — student to write before outcome is revealed

Define the observation reference, measurement method and checkpoints first. See section 7 of the instructor notes for an example; no validated trading setup is implied. Do not make scenario activation depend on a numerical consensus that cannot be verified.

Instructor-proposed measurement protocol, supplied before student scenarios: T = 08:30 New York. P0 will be the close of the one-minute interval 08:29:00–08:29:59; its numeric value is not yet recorded. The T+5 and T+15 observations will use completed closes of 08:34:00–08:34:59 and 08:44:00–08:44:59 respectively. Define expectations about these closes versus P0 before revealing the release. An above/below +0.2% condition refers only to the attributed preview benchmark. If equal to the benchmark, neither above/below condition activates. Conditions, direction and invalidation remain for the student to write; do not infer them from subsequent results.

### Scenario A — frozen v1

- Condition: August Core CPI month over month greater than the attributed +0.2% expectation benchmark (student submission, 2026-09-29).
- Evidence expected and evaluation window: Both completed closes at T+5 and T+15 strictly below P0. No requirement that every intervening bar decline. Operational rule developed with instructor guidance.
- Invalidation: If A activates, either observed checkpoint close greater than or equal to P0 contradicts this two-checkpoint prediction.
- Permitted action: Observe only.

### Scenario B — frozen v1

- Condition: August Core CPI month over month below the attributed +0.2% expectation benchmark (student submission, 2026-09-29).
- Evidence expected and evaluation window: Both completed closes at T+5 and T+15 strictly above P0. No requirement that every intervening bar rise. Operational rule developed with instructor guidance.
- Invalidation: If B activates, either observed checkpoint close less than or equal to P0 contradicts this two-checkpoint prediction.
- Permitted action: Observe only.

### Neither scenario / insufficient evidence

- Core CPI equal to +0.2%: neither above/below condition activates; not a forecast of an unchanged market.
- Missing release/price data: not assessable, not a successful or failed scenario.
- Distinguish a scenario not activated by the release from an activated scenario contradicted by the observed prices.

### Original student scenario submission — 2026-09-29, preserved verbatim

1. Avec un core CPI supérieur à 0.2 %, cela indique que les prix à la consommation ont augmenté plus que prévue. Si la valeur est fortement supérieure, la FED pourrait être enclin à augmenter le taux d'intérêt. Cela diminurait la capacité des entreprises à emprunter, donc signalerait une baisse de revenue potentiel. Le prix du MES diminuerais jusqu'en t + 15 avec un core cpi supérieure à 0.2%
2. Avec un core CPI inférieure, cela aurait l'effet inverse. Le prix du MES augmenterais jusqu'en t + 15

Coach review: coherent conditional directional hypotheses, not demonstrated causal facts. Core CPI concerns the consumption-price index excluding food and energy. Tightening expectations can raise financing costs and affect spending and asset valuations; they do not establish an immediate revenue decline for companies. Intraday prices can respond to revised expectations before any actual policy change or realized effect on businesses. The reverse directional case is plausible, not automatic. Source: [Federal Reserve — monetary-policy transmission](https://www.federalreserve.gov/monetarypolicy/monetary-policy-what-are-its-goals-how-does-it-work.htm), checked 2026-09-29.

Next: student states for each proposed two-checkpoint scenario the precise observation relative to P0 that would contradict it, treating equality explicitly. This is a price-scenario test over fifteen minutes, not a test proving the Fed/earnings causal chain. The replay should remain paused until the rules are finalized and saved. No final freeze or post-release observation inferred from this submission.

### Student invalidation attempt — 2026-09-29, preserved verbatim

1. Si les deux temps sont supérieure à P0.
2. Si les deux temps sont inféreurs à P0.
3. Si la cloture est exactement égale à P0, cela m'indiquerait que le marché est indiférent.

Coach assessment: the first two answers identify sufficient contradicting cases but omit mixed checkpoint outcomes and equality. Because success requires both strict inequalities, one contrary or equal observed close suffices to contradict the specified scenario. Equality establishes only zero net price change from P0 at that checkpoint, not market indifference, absence of volatility or balanced participant motives. Missing data remain not assessable; they are not equivalent to equality. These criteria concern the declared checkpoint prediction, not the truth of an entire macroeconomic mechanism.

Targeted fictional recheck, unrelated to the hidden replay outcome: assume A activates, P0 = 7600.00, T+5 close = 7598.00 and T+15 close = 7601.00. Ask whether A's checkpoint prediction is met and which checkpoint contradicts it. Then ask whether the conclusion changes if T+15 equals 7600.00. Student response pending; keep replay paused and final freeze pending.

### Recheck accepted and rules frozen — 2026-09-29

Student response, verbatim:

1. Non, la clôture à T + 15 est supérieure à P0
2. Non, car elle est égale à P0. La réaction attendu doit être inférieure.

Assessment: both answers correct. Student identifies a mixed checkpoint outcome and equality as contradictions of A's strict two-checkpoint criterion. Accept this clarification after coaching; B remains the instructor-assisted symmetric rule, not a separately examined unassisted response. Freeze the operational conditions, checkpoints and inequalities above as v1. Preserve prior attempts as history; their pending statements are superseded by this dated decision.

Frozen snapshot: `01-MES.pre-event-v1.md`. Subsequent publication facts, price readings and evaluation belong in the audit. P0's numerical value is still pending but its measurement interval is fixed. Do not change a condition or checkpoint after seeing the outcome. This is one coached observation protocol, not a validated trading edge. The earlier instructor search-exposure limitation remains documented.

### No-trade conditions

- All conditions: this is an observation exercise.

## Risk

- Maximum risk per trade: N/A — observation only.
- Daily stop: N/A — observation only.
- Maximum trades: 0.
- Event exclusions: Entire exercise excludes order submission.

## Evidence and checks

- Pre-event screenshot and exact chart timestamp: Saved and reviewed; replay start 08:25:00, latest displayed data 08:24:59 on 2026-09-11. Additional event/post-event evidence still pending.
- Reference price and its completed candle interval: P0 = close of 08:29:00–08:29:59; numeric value pending, to be observed only after scenarios are saved.
- Predefined post-event checkpoints: Completed one-minute closes ending 08:34:59 and 08:44:59 (T+5/T+15); instructor protocol, not a trading setup.
- Signed calculation recheck: Pending independent student calculation with verified inputs and units; do not fabricate a consensus to make this possible.
- Expiry-comparison recheck: Pending when comparable historical contract quotes are available; otherwise retain for a later brief.

## Post-session audit — append only after freezing the pre-event brief

- Audit date/time:
- Official release source, original publication time and actual figure:
- Surprise versus verified consensus, if available:
- Change versus previous reading (distinct from surprise):
- What occurred at each predefined checkpoint?
- Which scenario, if any, activated?
- What contradicted the original hypothesis?
- Did I use future information or already know the outcome?
- Screenshot/evidence links:
- Best process decision:
- Main error:
- One improvement:

Preserve the frozen pre-event snapshot. Append dated audit entries below; do not rewrite the scenarios to fit the outcome. At freeze, no numerical P0, post-event price observations, study duration or completed brief is recorded.
