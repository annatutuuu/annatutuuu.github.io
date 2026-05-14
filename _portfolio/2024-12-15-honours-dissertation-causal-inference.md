---
title: "Honours Dissertation - Standardization and IPW for Causal Inference"
collection: portfolio
section: undergrad_research
permalink: /portfolio/honours-dissertation-causal-inference/
date: 2024-12-15
project_period: "Sep 2024 - April 2025"
header:
  teaser: projects/DAG.png
excerpt: "Causal inference on smoking's effect on obesity risk using nonparametric and parametric IPW/standardization methods on 400K+ CDC survey records."
---

## Overview

Observational data cannot directly reveal causation — a smoker and a non-smoker differ in many ways beyond their smoking habit. This project applies causal inference methods to estimate the **Average Treatment Effect (ATE)** of current smoking on overweight/obesity risk (BMI > 25), using 400,000+ records from the CDC's 2023 BRFSS survey.

To formalize the causal question, I constructed a **Directed Acyclic Graph (DAG)** identifying confounders — age, education, veteran status, and number of children under 18 — that influence both smoking behavior and weight outcomes.

![DAG](/images/projects/DAG.png){: width="70%" }

## Identification & Assumptions

- Verified three core causal identification assumptions: **exchangeability** (no unmeasured confounding given L), **positivity** (all covariate strata contain both smokers and non-smokers), and **consistency** (treatment is well-defined and non-interfering).
- Justified conditional exchangeability through the DAG structure; confirmed positivity empirically across all covariate strata in the dataset.

## Nonparametric Estimation

- Because the dataset is observational, direct comparison between groups is biased. To recover the causal effect, I implemented **nonparametric standardization** and **Inverse Probability Weighting (IPW)** in R, adjusting for age as a single confounder.
- Both methods converged to ATE ≈ −0.088, suggesting smoking is associated with an 8.8 percentage point reduction in overweight probability after adjustment.
- Proved the mathematical equivalence of standardized means and IP-weighted means under consistency and conditional exchangeability.

## Parametric Estimation

- Extended both methods to adjust for all four confounders simultaneously using parametric models, addressing the data sparsity problem that arises with nonparametric stratification across multiple covariates.
- Estimated **propensity scores** via logistic regression; visualized score distributions by treatment group to confirm confounding and motivate the need for adjustment.
- Applied **parametric IPW** and **stabilized IPW**; obtained ATE = −0.0553 (95% CI: [−0.0583, −0.0523]), a smaller effect than the nonparametric estimate due to more comprehensive confounder adjustment.
- Fitted a **parametric standardization model** with treatment-covariate interaction terms; obtained ATE = −0.0929, with the discrepancy from IPW suggesting model misspecification in the outcome model.

## Limitations & Reflection

- Discussed sources of bias including unweighted sampling, complete-case selection bias, and omitted variable bias.
- The divergence between IPW and standardization estimates highlights the sensitivity of causal inference to model specification, motivating the use of **doubly robust estimators** as a future direction.
