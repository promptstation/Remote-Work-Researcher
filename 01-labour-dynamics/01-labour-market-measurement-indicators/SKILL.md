---
name: labour-market-measurement-indicators
description: Construct, interpret, audit, and report labour-market statistics using ILO/ICLS definitions, labour-force surveys, and comparable international sources. Use whenever the user asks about employment, unemployment, labour force participation, underemployment, informal work, joblessness, labour-market tightness, labour statistics, ILOSTAT, BLS/CPS indicators, U-3/U-6, LU1–LU4, employment-to-population ratios, hours worked, status in employment, or needs a labour-market diagnostic from data or a headline rate. Apply even if the user only pastes a percentage, asks "is unemployment high", compares countries, or wants a jobs briefing — this skill is required before interpreting any labour-market number.
compatibility: Works with public labour statistics, survey microdata descriptions, statistical releases, and research briefs; no proprietary software required. Prefer ILOSTAT, national labour-force surveys, BLS/CPS/JOLTS, Eurostat, and official statistical offices.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 01-labour-market-measurement-indicators
---

# Labour Market Measurement and Indicators

## Mission

Treat every labour-market number as a constructed object, not a fact of nature. Before interpreting employment, unemployment, participation, or "jobs," recover the definition, population, source, reference period, and comparability limits that produced the number.

A professional remote researcher does not report a rate. They report what the rate counts, who it excludes, which alternative measure would change the story, and whether the comparison the user wants is statistically valid.

Optimize simultaneously for:

- definitional fidelity to ILO/ICLS standards
- source fitness (survey vs establishment vs administrative vs modelled)
- comparability across time, countries, and groups
- honest uncertainty about breaks, coverage, and imputation
- a diagnostic that a policymaker or researcher can act on

Do not treat the unemployment rate as the labour market. Do not mix 13th ICLS and 19th ICLS employment concepts without saying so. Do not compare a seasonally adjusted monthly CPS figure to an annual ILO modelled estimate as if they were the same object.

## When this skill governs

Use this skill when the task involves:

- explaining or computing LFPR, employment-to-population ratio, unemployment, underemployment, inactivity, NEET, informal employment, or hours
- comparing labour markets across countries, years, sexes, ages, regions, or education groups
- reconciling conflicting headlines ("unemployment fell but jobs feel worse")
- choosing an indicator for a brief, dashboard, paper, or due-diligence note
- auditing someone else's labour statistic for definition or source error
- translating a national release into internationally comparable language

If the user wants causal labour-supply, demand, or policy analysis, still start here: get the stock and flow measures right before modelling them.

## Core output

Unless the user asks for a different artifact, deliver a **Labour Market Measurement Note** with:

1. **Question restated in measurable terms**
2. **Population and concept** (who is counted, which form of work, which labour-force status)
3. **Primary indicator(s)** with exact formula
4. **Companion indicators** that prevent a one-number story
5. **Source and vintage** (survey, establishment, admin, modelled; date; seasonal adjustment)
6. **Disaggregation** that matters for the question
7. **Comparability caveats** (definition change, age coverage, geography, ICLS revision, series break)
8. **Interpretation** — what the numbers can and cannot support
9. **What would change the conclusion**

Keep the note short enough to brief. Put formulas, classifications, and audit checks where they change the answer, not as decoration.

## Phase 1 — Recover the statistical object

Before any narrative, answer:

| Question | Why it matters |
| --- | --- |
| What is the population? | Working-age (often 15+, 15–64, or 16+) vs civilian non-institutional vs including armed forces |
| What is the reference period? | Week, month, quarter, year; "currently available" windows differ |
| What is the source? | Household LFS, establishment survey, administrative register, census, ILO modelled estimates |
| Which statistical standard? | 13th ICLS (1982) vs 19th ICLS (2013) employment and underutilization |
| Is it a stock, a flow, or a rate? | Employment level vs employment-to-population vs unemployment rate vs hires/separations |
| Seasonally adjusted or not? | Never mix SA and NSA in a short-run comparison |
| National or internationally harmonised? | Country release vs ILOSTAT vs OECD vs modelled |

If any cell is unknown, state the assumption. Do not silently inherit the user's wording ("unemployment is 5%") as a defined indicator.

## Phase 2 — Classify people, not jobs slogans

### Working-age population

Default international working-age population is persons aged 15 and over, unless the question is explicitly prime-age (25–54), youth (15–24), or a national legal definition. Never compute rates on total population when the denominator should be working-age.

### Labour-force status (mutually exclusive)

In the labour-force framework, every working-age person is exactly one of:

1. **Employed**
2. **Unemployed**
3. **Outside the labour force** (inactive)

**Labour force** = employed + unemployed.

These three statuses are not forms of work. Forms of work (19th ICLS) cut across a different axis.

### 19th ICLS forms of work

Work is any activity producing goods or services for use by others or own final use. Distinct forms:

- **Employment** — work for pay or profit
- **Own-use production work** — goods or services for own final use (including much subsistence production and unpaid domestic services)
- **Unpaid trainee work**
- **Volunteer work**
- **Other work activities**

Under the 19th ICLS, producing goods solely for own consumption is **not employment**. Under the 13th ICLS it often was. This single revision can move large shares of rural and female work out of employment and into own-use production. When a series or a country comparison straddles the revision, treat it as a possible series break, not a labour-market miracle.

### Employment

Employed persons are working-age persons who, in the reference period, worked for pay or profit (including temporarily absent from such a job). Include:

- employees, employers, own-account workers, contributing family workers in market units
- persons with a job but temporarily not at work (subject to national operational rules)

Do not equate "has work" with "has a decent job." Employment is a status, not a quality measure.

### Unemployment (standard / LU1)

Unemployed persons are working-age persons who simultaneously:

1. were **not in employment**
2. **sought** employment in a recent specified period
3. were **currently available** to start

All three tests are required. Dropping "seeking" produces a different object (often closer to the potential labour force). Dropping "available" does too. Never call a jobless person unemployed without the search-and-availability tests unless you are explicitly using a broader underutilization measure.

### Outside the labour force

Includes students, retirees, discouraged jobseekers, unpaid carers, and others not employed and not unemployed. This is not "idle" and not "unproductive." Own-use production and unpaid care often sit here under 19th ICLS employment rules.

### Potential labour force

Persons not in the labour force who are:

- seeking but not available, or
- available but not seeking (including discouraged workers)

Potential labour force is the bridge between inactivity and unemployment. It is part of LU3 and LU4, not of the official unemployment rate.

## Phase 3 — Construct the indicator set, never a lone rate

Compute or report this core set unless the user forbids it.

### Levels

- Working-age population \(WAP\)
- Employed \(E\)
- Unemployed \(U\)
- Labour force \(LF = E + U\)
- Outside the labour force \(OLF = WAP - LF\)
- Time-related underemployed \(TRU\)
- Potential labour force \(PLF\)
- Extended labour force \(ELF = LF + PLF\)

### Rates (always state the denominator)

**Labour force participation rate**

\[
LFPR = 100 \times \frac{LF}{WAP}
\]

**Employment-to-population ratio** (employment rate in ILO usage)

\[
EPR = 100 \times \frac{E}{WAP}
\]

**Inactivity rate**

\[
IR = 100 - LFPR
\]

**Unemployment rate (LU1)**

\[
LU1 = 100 \times \frac{U}{LF}
\]

**LU2 — unemployment + time-related underemployment**

\[
LU2 = 100 \times \frac{TRU + U}{LF}
\]

**LU3 — unemployment + potential labour force**

\[
LU3 = 100 \times \frac{U + PLF}{ELF}
\]

**LU4 — composite labour underutilization**

\[
LU4 = 100 \times \frac{TRU + U + PLF}{ELF}
\]

**NEET** (youth not in employment, education, or training)

\[
NEET = 100 \times \frac{\text{youth not employed and not in education/training}}{\text{youth population}}
\]

### Identity that prevents false stories

\[
EPR = LFPR \times (1 - LU1/100)
\]

If unemployment falls while EPR is flat, participation fell. If unemployment is low but EPR is low, the labour market is not absorbing the working-age population. Always pair LU1 with EPR and LFPR.

### Hours and volume

When the question is about labour input, not headcount:

- mean weekly hours actually worked per employed person
- total weekly hours
- full-time equivalent jobs (total hours / 40 or 48, and state which)

Headcount employment can rise while hours fall. Do not call that a jobs boom without hours.

### US-specific mapping (only when the data are US)

- U-3 ≈ ILO LU1 (official unemployment)
- U-4 adds discouraged workers
- U-5 adds other marginally attached
- U-6 adds involuntary part-time (related to, not identical to, LU2)

Do not paste U-6 into a non-US comparison as if it were LU4.

## Phase 4 — Choose the source on purpose

### Household labour-force survey (preferred default)

Best for: labour-force status, unemployment, participation, informal work, multiple jobholding, hours actually worked, demographic detail.

Limitations: sampling error, undercount of some informal or unpaid work if probing is weak, delayed release, breaks when questionnaires or ICLS standards change.

### Establishment / payroll survey

Best for: non-farm payroll jobs, industry detail, earnings of employees, short-run jobs pulse.

Limitations: counts **jobs** not **people**; misses much self-employment, agriculture, and informal units; cannot produce unemployment or LFPR; benchmark revisions.

### Administrative data (UI claims, tax, social security)

Best for: high-frequency flows, registered unemployment, formal wage bills.

Limitations: coverage equals the rules of the programme. Registered unemployment is not ILO unemployment. Claims are not the unemployment rate.

### Population census

Useful for small-area structure. Usually understates labour-force activity relative to a dedicated LFS because of limited probing.

### ILO modelled estimates (ILOEST)

Use for: cross-country panels, global/regional aggregates, filling missing country-years.

Do not treat them as a national official series. They benchmark population to UN WPP, may impute, may smooth, and can differ from the national statistical office. Always label "ILO modelled estimate" with the vintage.

### Source-selection rule

- One country, official current reading → national LFS (or CPS) first
- Jobs in formal firms, month-to-month → establishment/payroll
- Cross-country research → ILOSTAT, documenting 13th vs 19th ICLS and modelled vs reported
- Informality, own-use production, time-related underemployment → LFS micro or ICLS-compliant modules, not payroll data
- Tightness / vacancies → vacancy survey or JOLTS plus unemployment, never unemployment alone

If two sources disagree, explain the object each measures. Do not average them.

## Phase 5 — Classify jobs once people are classified

After labour-force status, describe **what employed people do**.

### Status in employment (ICSE)

Distinguish:

- employees
- employers
- own-account workers
- contributing family workers
- and, where available, dependent contractors (relevant for platform work)

A rise in employment that is entirely contributing family workers or own-account work in subsistence-adjacent activities is not the same as a rise in wage employment.

### Industry (ISIC) and occupation (ISCO)

Use 1-digit structure for structural change (agriculture / industry / services). Use more detail only when sample size supports it. Do not infer occupation quality from industry, or industry from occupation.

### Informal employment

Informal employment is a **job-based** concept: employment relationships not covered (in law or in practice) by formal arrangements. Informal sector is an **enterprise-based** concept. A person can hold informal employment in a formal firm.

Never use "informal sector share" as a synonym for "informal employment share."

When informality is the question, payroll surveys are the wrong source.

### Time-related underemployment

Requires all of:

1. employed
2. wants additional hours
3. worked below a hours threshold
4. available to work additional hours

Part-time is not underemployment. Voluntary short hours are not LU2.

## Phase 6 — Disaggregate before you generalise

A national rate that is not split at least by **sex** and **age** is usually incomplete. Add, when the question or data allow:

- rural / urban
- education
- disability
- nationality / migrant status
- formal / informal
- status in employment
- industry and occupation
- region

Prime-age (25–54) EPR is often the cleanest cyclical measure because it is less distorted by schooling and retirement. Youth unemployment is sensitive to participation in education — pair it with NEET and youth EPR.

Do not "control" by dropping women, informal workers, or agriculture to make a market look standard. If those groups are the labour market, they stay in the frame.

## Phase 7 — Interpret with companion indicators

Use this diagnostic grid.

| Observation | Do not conclude | Check instead |
| --- | --- | --- |
| Unemployment rate fell | The labour market improved | Did EPR rise or did LFPR fall? Did hours rise? Did LU4 fall? |
| Unemployment is low | Full employment / healthy market | EPR, LU2–LU4, informality, working poverty, wage growth |
| Employment rose | More people in decent jobs | Headcount vs hours; status in employment; informal share; payroll vs household |
| LFPR fell | People "don't want to work" | Ageing, schooling, care burdens, discouragement (PLF), 19th ICLS reclassification |
| Women's LFPR is low | Low labour input | Own-use production, unpaid care, measurement of contributing family work |
| Country A unemployment < Country B | A is healthier | EPR, informality, social-insurance coverage, definition alignment |
| Payroll jobs and household employment diverge | One source is wrong | They measure different objects; inspect self-employment, multiple jobs, population controls |
| Series jumps in one year | Structural break in the economy | Questionnaire, ICLS revision, age coverage, geographic coverage, modelled vintage |

Write the interpretation as a comparison of **levels, changes, and composition**, not as a moral judgment about workers.

## Phase 8 — Comparability and series-break audit

Before any time-series or cross-country claim, run this audit:

1. **Age coverage** — 15+ vs 15–64 vs 16+ vs 15–72. Harmonise or disclose.
2. **ICLS standard** — 13th vs 19th. Especially material for agriculture, own-use production, and female employment.
3. **Geographic coverage** — national vs urban; inclusion of occupied territories, camps, or institutions.
4. **Civilian vs including armed forces**
5. **Seasonal adjustment**
6. **Reference period and frequency**
7. **Source switch** — census year vs LFS vs modelled splice
8. **Questionnaire or sampling redesign**
9. **Population benchmark revision** (UN WPP vintage for modelled series; CPS population controls)
10. **Classification revisions** — ISIC, ISCO, ICSE

If a break is likely, do not draw a trend through it. Report pre-break and post-break, or use overlapping observations.

For modelled series, state that missing country-years are imputed and that national official figures may differ.

## Phase 9 — Research workflow for a real request

### A. Headline or single number

1. Identify the producing agency and exact series name.
2. Recast it in ILO language.
3. Attach EPR, LFPR, and at least one underutilization companion.
4. State who is excluded.
5. Answer the user's question with the reconstructed object.

### B. Country diagnostic

1. Working-age definition and population structure (ageing can move LFPR without any behaviour change).
2. LFPR, EPR, LU1–LU4 by sex and age.
3. Employment composition: status, sector, occupation, informal share, hours.
4. Whether the binding problem is joblessness, low hours, low-quality/informal work, or non-participation.
5. One paragraph on data fitness.

### C. Cross-country or panel comparison

1. Prefer a single database and vintage.
2. Restrict to a common concept (do not mix 19th ICLS employment with 13th ICLS employment).
3. Prefer EPR and LFPR alongside LU1.
4. Flag countries whose LFS does not cover agriculture, informal, or own-use production well.
5. Do not rank countries on LU1 alone.

### D. Reconciling conflicting series

Set out a table: concept, unit (persons vs jobs), coverage, frequency, adjustment, latest value, direction of change. Then explain the discrepancy as a difference in objects. Only after that consider measurement error.

## Phase 10 — Writing standard

Use precise nouns: persons employed, employees, jobs, hours, labour force, potential labour force. Do not write "the unemployed" when you mean "the jobless," or "employment rate" when you mean the unemployment rate.

When you must use a national nickname (U-3, claimant count, registered unemployment, EPOP), define it once in ILO terms.

Quantify. "Unemployment is high" is not an output. "LU1 is 12.4% of the labour force; EPR is 51%; LU4 is 23%" is an output.

Separate:

- **what the data measure**
- **what they suggest**
- **what they cannot decide** (job quality, well-being, causality)

## Anti-patterns

Do not:

- treat LU1 as a sufficient statistic of labour-market health
- call discouraged workers unemployed in the official rate
- call all part-time work underemployment
- call own-use production "unemployment" or "inactivity" without the 19th ICLS distinction
- compare payroll jobs to household employment without translating units
- compare registered/claimant unemployment to ILO unemployment
- use establishment data to measure informality or self-employment
- drop agriculture to "clean" a developing-country series
- interpret a 19th ICLS implementation as a collapse in employment
- mix SA and NSA, monthly and annual, modelled and official, without labels
- report youth unemployment without NEET or youth EPR
- use total population as the denominator of LFPR or EPR
- claim "full employment" from a low unemployment rate when EPR is weak or LU4 is high
- average incompatible series
- moralise non-participation

## Decision heuristic

Before locking the indicator, ask:

1. Is the question about **people**, **jobs**, **hours**, or **income**?
2. Is the relevant status **employment**, **unemployment**, **underutilization**, or **non-participation**?
3. Which denominator makes the rate answer the question?
4. What companion indicator would falsify the headline story?
5. Can this comparison survive an ICLS, age, and source audit?
6. What group is hidden in the aggregate?

If you cannot answer (1)–(3), you are not ready to report a number.

## Validation gate

Before delivery:

- every rate has a named numerator and denominator
- LU1 is never presented as the only labour-market indicator unless the user insisted, in which case the limitation is stated
- EPR and LFPR appear whenever unemployment is discussed
- source, vintage, and adjustment are named
- 13th vs 19th ICLS is addressed if employment levels or rural/female series are in play
- disaggregation by sex and age is present or explicitly impossible
- informal, hours, or status composition is addressed when "job quality" or developing-country markets are in play
- no comparison crosses a known series break without a flag
- claims of improvement or deterioration are supported by more than one indicator
- language distinguishes persons, jobs, and hours

## Final principle

The labour market is a set of statuses, volumes, and classifications. Measurement is the skill of keeping those objects distinct. A researcher who reports one rate has not measured the labour market; they have repeated a headline. The professional standard is a small, consistent system of indicators that cannot be gamed by moving people between employment, unemployment, and inactivity without being seen.
