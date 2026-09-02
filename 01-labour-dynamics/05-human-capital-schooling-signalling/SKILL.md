---
name: human-capital-schooling-signalling
description: Analyze education, training, and skills as labour-market investments — Mincer earnings, returns to schooling, Ben-Porath life-cycle investment, general vs specific training, credit constraints, and Spence signalling. Use whenever the user asks whether education pays, how to estimate returns to schooling, whether a degree is just a signal, who should receive training, or how schooling changes wages and employment. Apply even if they only ask "is college worth it" or want a skills-gap briefing.
compatibility: Works with earnings microdata descriptions, education statistics, and published return-to-schooling estimates.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 05-human-capital-schooling-signalling
---

# Human Capital, Schooling, Training, and Signalling

## Mission

Treat schooling and training as investment decisions under uncertainty, not as automatic wage machines. Separate productivity-enhancing human capital from signalling. Estimate or interpret returns with the selection problem in view. Never report a Mincer coefficient as "the causal return to education" without saying how identification was attempted.

## When this skill governs

Use for returns to education, training programmes, on-the-job learning, sheepskin effects, overeducation, skills gaps, credit constraints on schooling, and whether credentials raise wages because they teach or because they sort.

## Core output

Deliver a **Human Capital Note**:

1. Investment object (years of school, credential, general training, specific training)
2. Costs (direct, forgone earnings, effort) and expected benefits (wage path, employment, amenities)
3. Working theory (human capital, signalling, or both)
4. Empirical return and identification
5. Heterogeneity (who benefits)
6. Policy implication that survives the identification caveat

## Phase 1 — Human capital as investment

Becker: people invest until the marginal return equals the marginal cost. Costs are tuition plus forgone earnings plus psychic cost. Benefits are the discounted gain in future earnings and employability.

Implications:

- younger people invest more (longer horizon)
- higher ability and lower discount rates raise investment
- credit constraints can produce under-investment relative to the social or private optimum
- compulsory schooling and subsidies change the cost side

Do not treat "more education is always better" as an implication of the theory. The theory is about optimal investment, including corner solutions.

## Phase 2 — Mincer equation and what it is not

The workhorse log-earnings equation:

\[
\ln w = a + rS + bX + cX^2 + \varepsilon
\]

where \(S\) is years of schooling and \(X\) is experience.

\(r\) is a descriptive return, not automatically causal. Ability bias, comparative advantage, measurement of schooling, and compensating differentials all sit in \(\varepsilon\).

Experience-earnings profiles are concave if investment declines over the life cycle (Ben-Porath). Do not interpret the quadratic as a law of nature; it is a convenient shape for declining on-the-job investment.

When you report a Mincer \(r\):

- say OLS vs IV vs RDD vs twins vs panel
- say the instrument if IV (compulsory schooling, distance, quarter of birth — each has a local LATE)
- say whether the return is to years or to a credential

## Phase 3 — Signalling

Spence: education can raise wages by revealing ability even if it does not raise productivity.

Diagnostics that lean toward signalling:

- sheepskin (diploma) discontinuities larger than the implied year effects
- employer learning that flattens education coefficients with experience
- credentials that are costly to obtain but weakly tied to job tasks

Diagnostics that lean toward human capital:

- returns in self-employment and in occupations where output is directly observed
- curriculum content that maps to task productivity
- training that raises measured productivity inside firms

Most labour markets mix both. Do not pick a side as a worldview. Ask which share of the return is likely productive for this credential and this occupation.

## Phase 4 — General vs specific training

- **General training** raises productivity in many firms. In a competitive labour market the worker pays (lower wage during training) and captures the return.
- **Specific training** raises productivity only here. Firm and worker share costs and returns; turnover risk limits investment.

Implications:

- poaching and turnover cut specific training
- minimum wages can cut jobs that were training-and-low-wage packages
- public training programmes must specify whether they produce general skills and who captures the return

Do not call every firm course "human capital policy." If the skill is not portable and the firm captures the rent, it is a firm investment, not a worker earnings policy.

## Phase 5 — Heterogeneity and selection

Returns differ by:

- level (primary vs secondary vs tertiary vs postgraduate)
- field of study
- quality of institution
- gender and group (discrimination and hours interact — do not dump the gap into "education")
- local labour demand for the skill

Selection: people who study more would often have earned more anyway. LATE from compulsory-schooling instruments is not the return to an extra year of MBA. Match the estimate to the policy.

Credit constraints and information frictions matter more at the margin of college entry in some countries than in others. Do not import a US college-returns debate into a setting where the binding margin is completing primary school.

## Phase 6 — Education production and skills gaps

"Skills gap" is not a measured object until you specify the skill, the job, the wage, and the time to train.

A true shortage: wages and vacancies in that occupation rising together, training pipelines lagging.

A fake shortage: firms wanting cheaper workers with more credentials, or a matching/geographic problem, or a compensating-differential problem.

School quality and education production (class size, teacher effects) affect the human-capital content of a year of \(S\). Years are not interchangeable across systems.

## Phase 7 — Research workflow

1. Name the investment and the alternative (what the person would do instead).
2. Write costs and the expected earnings path.
3. Choose human capital, signalling, or a split.
4. Select an empirical return with identification that matches the policy margin.
5. Inspect heterogeneity and selection.
6. Translate into a decision (invest / do not / redesign the programme).

## Anti-patterns

- Reporting OLS Mincer coefficients as causal
- Treating all education returns as signalling or none as signalling
- Using a college LATE to justify early-grade policy, or vice versa
- Calling every vacancy a skills gap
- Ignoring forgone earnings in "is college worth it"
- Equating years of schooling across unequal systems
- Ignoring general vs specific when designing training subsidies

## Decision heuristic

1. What is being invested in?
2. Does it raise productivity, reveal productivity, or both?
3. Whose return — worker, firm, or society?
4. Which causal estimate matches this margin?
5. What is the next-best use of the person’s time?

## Validation gate

- Investment object named
- Costs include forgone earnings
- Theory (HC vs signal) explicit
- Empirical return has an identification sentence
- Heterogeneity acknowledged
- Policy claim does not outrun the LATE

## Final principle

Education is an investment with a selection problem. The professional standard is to say what was purchased, what it did to productivity versus information, and whose causal return you actually have.
