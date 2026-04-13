# Part 69: Causal Inference in Marketing — Moving Beyond Correlation

## Learning Objectives
- Understand the fundamental problem of causal inference and why it matters for marketing decisions
- Apply key causal inference frameworks: potential outcomes, DiD, synthetic control, IV, and RDD
- Use Google CausalImpact for campaign analysis in practice
- Identify when causal methods change marketing decisions vs. when correlation suffices
- Build organizational capability for causal thinking in marketing teams

---

## The Fundamental Problem

Every marketing organization faces a version of the same question: **did this campaign actually cause revenue to increase, or would sales have risen anyway?**

Correlation-based analysis — comparing performance before and after a campaign, or between high-exposure and low-exposure groups — cannot answer this question. It confounds the marketing effect with selection bias, seasonality, and macro trends.

**The fundamental problem of causal inference (Holland, 1986):** we cannot observe the same unit in both treated and untreated states simultaneously. A customer either saw the ad or didn't. We observe only one potential outcome; the other is a counterfactual.

This is not a data problem. It is a logical constraint. The entire science of causal inference is a set of principled methods for constructing credible counterfactuals.

---

> **Research Gap**
>
> Causal inference methods borrowed from econometrics assume marketing interventions and outcomes are well-defined and measurable — in practice, brand marketing effects are diffuse and long-delayed, making clean causal identification extremely difficult and rarely achieved in published research. The field lacks a coherent methodological framework for causal attribution of brand equity effects, where the treatment (brand advertising) is continuous, the outcome (brand perception, consideration) is measured with error, and the lag between intervention and economic effect can span years.

---

## The Potential Outcomes Framework

The **Rubin Causal Model** formalizes causal inference around potential outcomes:

- **Y(1)** = the outcome unit *i* would experience if treated
- **Y(0)** = the outcome unit *i* would experience if not treated
- **Individual treatment effect** = Y(1) − Y(0)
- **Average Treatment Effect (ATE)** = E[Y(1) − Y(0)] across the population

The challenge: we only ever observe Y(1) for treated units and Y(0) for control units. The unobserved counterfactual must be **imputed** through randomization (experiments) or **estimated** through quasi-experimental methods.

**Key identification assumptions** that most methods require:
- **SUTVA** (Stable Unit Treatment Value Assumption) — treatment of one unit doesn't affect another
- **Ignorability** — conditional on observed covariates, treatment assignment is independent of potential outcomes
- **Overlap** — treated and control units share common support in the covariate distribution

---

## Key Methods in Marketing Causal Inference

### Difference-in-Differences (DiD)

DiD compares the change in outcomes over time between a treatment group and a control group. The "difference in differences" removes time-invariant confounders.

**Marketing applications:**
- Estimating the impact of entering a new advertising channel
- Measuring the effect of a pricing change in select markets
- Evaluating the impact of a rebrand on customer acquisition in treated regions

**Critical assumption: parallel trends** — in the absence of treatment, the treatment and control groups would have followed the same trajectory. Violations (e.g., treatment group was growing faster pre-treatment) invalidate the estimate.

**Event study plots** — visualizing pre-treatment trends — are essential for credibility.

### Synthetic Control

When no single comparison unit is a clean control, synthetic control constructs a weighted combination of control units that best matches the treatment unit's pre-treatment trajectory.

**Marketing applications:**
- "What would sales have been in California if we hadn't run the brand campaign there?"
- Evaluating the impact of sponsorship activations in specific markets
- National launch impact analysis using non-launch markets as synthetic controls

The method requires a reasonably long pre-treatment period (typically 12+ months) and a pool of plausible comparison units.

### Instrumental Variables (IV)

IV methods exploit an external variable (the "instrument") that affects treatment assignment but has no direct effect on the outcome — allowing estimation of a causal effect even when selection into treatment is endogenous.

**Marketing instrument examples:**
- **Weather** as an instrument for store visits (weather affects foot traffic but doesn't directly cause purchases)
- **Competitor ad outages** as instruments for own-brand ad exposure
- **Platform algorithm changes** as instruments for organic reach

IV is technically demanding and requires strong justification for the exclusion restriction. Weak instruments (low correlation with treatment) produce unreliable estimates.

### Regression Discontinuity Design (RDD)

RDD exploits a threshold in an assignment rule: units just above a cutoff are in the treatment group; units just below are in the control group. At the threshold, treatment is as-good-as-randomly assigned.

**Marketing applications:**
- Evaluating loyalty program tier-upgrade effects (customers who just crossed a spend threshold vs. those just below)
- Measuring the impact of promotional eligibility cutoffs
- Price promotion threshold effects

### Google CausalImpact

CausalImpact (Brodersen et al., 2015) is an R package that uses Bayesian structural time series to estimate the causal effect of an intervention on a time series outcome.

**Workflow:**
1. Identify the intervention date (campaign launch, feature release)
2. Select control time series (channels not exposed, correlated markets)
3. Fit a structural time series model on the pre-intervention period
4. Use the model to predict the counterfactual post-intervention
5. The causal effect = observed − counterfactual, with credible intervals

CausalImpact is widely used in marketing analytics because it requires only time series data — no experimental design — and produces intuitive visualizations.

---

## Practical Applications: When Causal Methods Change Decisions

| Business Question | Default (Correlational) Answer | Causal Inference Answer |
|---|---|---|
| Did our Q4 TV campaign drive revenue? | "Revenue rose 18% during campaign period" | DiD vs. control markets: 6% attributable to campaign |
| Does our loyalty program increase LTV? | "Loyalty members spend 3x more" | RDD at tier boundary: 12% incremental spend effect |
| Did entering paid search increase overall demand? | "Paid search drives 25% of conversions" | Holdout geo: 8% true incrementality |
| Does email frequency affect unsubscribes? | "High-frequency segments have lower open rates" | IV / randomized send frequency: 2% churn increase per additional email/week |

---

## Frontier Signals

- **Uber's causal inference team** (2022–2024) has published multiple papers on applying DiD and synthetic control to evaluate surge pricing, driver incentives, and marketing campaigns — treating causal estimation as a product, not a research exercise
- **DoorDash's experimentation platform** incorporates CausalImpact for non-randomizable interventions, with automated parallel trends tests for DiD credibility
- **Microsoft Research's DoWhy** (Python) — open-source library that unifies potential outcomes and DAG-based causal reasoning, increasingly adopted by marketing data science teams
- **EconML (Microsoft)** — causal ML library supporting heterogeneous treatment effect estimation, allowing marketers to ask "for whom did this campaign work?"
- **Academic signal**: A 2023 Journal of Marketing paper by Goldfarb and Tucker reviewed 20 years of digital advertising causal studies, finding that the majority of identified effects are substantially smaller than correlational analyses suggest

---

## Building Causal Inference Capability in Marketing Teams

Most marketing teams are fluent in dashboards and attribution but lack causal reasoning infrastructure. Building capability requires:

**Tooling:**
- Deploy Google CausalImpact and DoWhy in the analytics environment
- Create templates for DiD and synthetic control in standard data science toolkits

**Process:**
- Add a "causal design review" step before major campaigns — what is the counterfactual? How will we know if it worked?
- Train analysts to distinguish correlation from causation in reporting

**Culture:**
- Reward honest "the campaign had no detectable causal effect" findings — suppressing null results leads to systematic overconfidence
- Build a library of past causal analyses so institutional knowledge accumulates

---

## Key Takeaways

- **Correlation is not causation** — but causal inference methods give us principled ways to approximate causation from observational data
- **DiD, synthetic control, IV, and RDD** are the core quasi-experimental toolkit for marketing contexts
- **Google CausalImpact** is the most accessible entry point for time series causal analysis in marketing
- **Brand effects are the hardest causal identification problem** — diffuse, lagged, and measured with error
- **Causal thinking is a culture change** as much as a technical upgrade — the goal is marketing decisions anchored in credible effect estimates, not flattering correlations

---

## Related Parts

- **Part 67** — Marketing Mix Modeling (causal inference as the foundation of MMM)
- **Part 68** — Incrementality Testing at Scale (randomized experiments as causal gold standard)
- **Part 70** — Customer Lifetime Value Frontier (causal LTV estimation)
- **Part 47** — Marketing Analytics Infrastructure
- **Part 44** — Attribution Modeling
