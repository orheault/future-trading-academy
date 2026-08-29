# Sierra Chart Setup Plan

**Status:** Safe training baseline; exact settings to be recorded during labs  
**Rule:** Simulation only until the curriculum explicitly changes status

## 1. Safety before configuration

- Confirm the selected trade account before every order-entry exercise.
- Keep live routing unconfigured during the foundations phase.
- Make the simulation status visually obvious.
- Learn `Cancel All`, `Flatten`, and Trade Activity Log reconciliation before any execution practice.
- Do not store credentials in this project.

## 2. Chartbook architecture

### `01-CONTEXT`

Purpose: clean price structure and session context.

- MES intraday chart;
- regular and overnight session boundaries;
- prior-day high/low and overnight high/low;
- opening range only when required;
- ATR or a simple volatility measure;
- no footprint display.

### `02-PROFILE`

Purpose: TPO and volume-at-price context.

- daily TPO profile with verified session times;
- 30-minute TPO subperiods for the standard learning configuration;
- TPO POC/value and Initial Balance;
- Volume by Price with VPOC/value;
- optional five-day or hypothesis-defined composite profile.

### `03-ORDER-FLOW`

Purpose: execution evidence.

- minimal Numbers Bars display;
- clearly documented bid/ask and imbalance settings;
- cumulative delta only if its calculation is documented;
- Time & Sales window;
- no decorative indicators.

### `04-EXECUTION-SIM`

Purpose: order entry and risk control.

- simulation account only;
- Trade DOM or chart-trading interface;
- bracket/OCO template;
- visible quantity, stop distance, and account name;
- daily loss controls when supported;
- Trade Activity Log accessible.

## 3. Data and session checks

Before using any chart for evidence:

1. confirm symbol and contract month;
2. confirm tick size and price display format;
3. confirm time zone;
4. confirm regular/evening session definitions;
5. confirm data continuity for the research period;
6. confirm whether data is delayed or real time;
7. confirm whether historical market depth is available;
8. document any missing data or replay limitation.

## 4. Replay workflow

1. Use an intraday chart with sufficient data loaded.
2. Select a start date without viewing future bars.
3. Use Trade Simulation Mode.
4. Clear or isolate prior simulated trade data for the symbol/account.
5. Use a realistic replay speed during decision windows.
6. Record whether actual bid/ask or estimated replay bid/ask is being used.
7. Do not assume DOM depth is historical unless depth data was recorded and is available.
8. Reconcile fills in Trade Activity Log after the session.

## 5. Internal versus server-based simulation

| Mode | Best use | Important limitation |
|---|---|---|
| Internal Trade Simulation | Chart replay and local practice | No server account balance tracking in the internal mode |
| Simulated Futures Trading Service | Forward paper trading and realistic account tracking | It is a separate server-based environment; replay uses internal simulation behavior |

Use current Sierra Chart documentation because service packages, data arrangements, and menu details can change.

## 6. Configuration record

Complete during Weeks 4, 7, 8, and 10:

| Item | Setting | Date verified | Reason |
|---|---|---|---|
| Time zone |  |  |  |
| MES session times |  |  |  |
| Data service |  |  |  |
| Replay mode |  |  |  |
| TPO profile period | 1 day candidate |  | Curriculum baseline |
| TPO subperiod | 30 minutes candidate |  | Standard learning baseline |
| TPO value area % |  |  | Record platform default/choice |
| Volume value area % |  |  | Record platform default/choice |
| Numbers Bars text type |  |  |  |
| Imbalance threshold |  |  | Must be tested, not assumed |
| Bracket stop/target |  |  | Must follow active setup |
| Sim account |  |  | Never record credentials |

## 7. Backup protocol

- Save chartbooks after material changes.
- Export or copy a dated configuration backup after each phase gate.
- Store screenshots with `YYYY-MM-DD_instrument_session_description.png` names.
- Record setting changes in `CHANGELOG.md` when they affect research comparability.

