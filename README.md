# Brazil's Economic Record: Bolsonaro (2019–2022) and Lula III (2023–)

ESTEEM Business Analytics: final-project dashboard (Week 11, *Designing Dashboards for Decision-Making*)
Team: Bernardo Moreira, Elisa Damascena, Jack O'Connell

### ▶ [Open the live dashboard](https://joconne8.github.io/brazil-economy-dashboard/)

The dashboard is one self-contained HTML file with plotly.js embedded. It also works offline: download `index.html` and open it in any browser. It needs no server and no account, and it works on a phone.

## Files

| File | What it is |
|---|---|
| [`index.html`](index.html) | The interactive dashboard |
| [`Dashboard Spec Template.docx`](Dashboard%20Spec%20Template.docx) | Our one-page spec, completed before any prompt was written |
| [`Brazil Economic Dashboard — Data for Jack.xlsx`](Brazil%20Economic%20Dashboard%20%E2%80%94%20Data%20for%20Jack.xlsx) | The dataset. The dashboard is built from the *Series observations* sheet. *Read me* and *Series guide* give definitions, sources and interpretation rules. |

## The spec in brief

- **Decider:** an undecided Brazilian voter who weighs jobs and take-home purchasing power.
- **Decision and cadence:** which economic record better fits their priorities. Checked monthly as new data arrive, and again before voting.
- **Headline:** the change in average real monthly earnings over each term, calculated as end ÷ start − 1. It covers employed people aged 14+ and is not household income.
- **Views:**
  1. Activity, jobs and earnings
  2. Inflation and interest rates
  3. Public finances
- **Controls:** administration, indicator, calendar dates vs. equal time in office, and a date-range slider. All controls are linked to every chart and every KPI card.
- **Deliberately out:**
  - a single "best president" score
  - voting advice
  - forecasts
  - claims that a president alone caused the changes
  - state-level data
  - combining fiscal measures that have different institutional coverage

## Default headline values

| | Window | Real earnings | Unemployment | 12-month IPCA |
|---|---|---|---|---|
| Bolsonaro | Dec 2018 → Dec 2022 (n = 48) | **−1.0%** (R$3,357 → R$3,324) | −3.8 pp | +2.04 pp |
| Lula III | Dec 2022 → Sep 2026 (n = 45, term in progress) | **+14.0%** (R$3,324 → R$3,790) | −2.7 pp | −1.21 pp |

Under "Equal time in office" (first 36 months of each term), real earnings changed by −8.4% under Bolsonaro and +12.8% under Lula III. Each term starts from the value it inherited. The n figures count monthly readings, which come from overlapping 3-month survey windows rather than independent samples.

## Honesty rules the dashboard follows

- Line axes start at zero. The one exception is real earnings, whose axis is zoomed and labelled on the chart. Every axis range is fixed, so no filter, toggle or slider rescales it.
- Every tooltip shows its n, unit, reporting frequency and source series. Every KPI card states its window and n.
- There are no pies, gauges or 3-D charts. Chart titles state findings in neutral, non-causal language.
- Gross debt (general government) is never combined with the fiscal balances (consolidated public sector).
- 2026 is marked as a partial year.

## Sources

- IBGE SIDRA: PNAD Contínua (earnings, unemployment), IPCA, quarterly national accounts.
- Banco Central do Brasil SGS: SELIC target, gross debt, primary and nominal balances.

The data were extracted on 2026-11-12 (UTC). They are latest-vintage series, not what voters could see at the time.

*The dashboard was built with an AI assistant from the spec above, then iterated and checked against the workbook.*
