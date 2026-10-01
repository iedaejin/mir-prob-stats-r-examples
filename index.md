---
layout: default
title: R examples
---

# R examples

Probability and Statistics (for Policy Analysis), MIR, SPEGA, IE University, Term 1, SEP-2026 S-2.

Prof. Dae-Jin Lee, daelee@faculty.ie.edu, IE University — Scitech.

Each session is one folder. Open that folder in RStudio and knit the files in the order below. Knit from inside the folder, so `read_csv("data/...")` finds the CSV that sits next to the script.

## Once, before the first knit

```r
install.packages(c("rmarkdown", "knitr", "tidyverse", "devtools"))
devtools::install_github("kosukeimai/qss-package")
```

Sessions 1 and 2 load datasets with `library(qss)`. Later sessions use the CSV in that session's `data/` folder. Those CSV files are course examples. They are not the QSS authors' files. The QSS files used in the Posit Cloud labs are in [mir-prob-stats](https://github.com/iedaejin/mir-prob-stats).

Run the chunk, then say what the number means. A slope, a p-value, or an interval does not by itself make the claim causal.

Sessions 8, 15, and 21–22 are exams and have no new files.

Source of this site: [github.com/iedaejin/mir-prob-stats-r-examples](https://github.com/iedaejin/mir-prob-stats-r-examples).

## Session 1 — Introduction

Datasets come from the `qss` package (`UNpop`).

- [01-setup.Rmd](01-introduction/01-setup.Rmd) — Install and load packages
- [01-arithmetic.Rmd](01-introduction/01-arithmetic.Rmd) — Calculator
- [01-unpop.Rmd](01-introduction/01-unpop.Rmd) — UN population: rows, columns, one summary
- [01-objects.Rmd](01-introduction/01-objects.Rmd) — Named objects
- [01-vectors.Rmd](01-introduction/01-vectors.Rmd) — A vector of world population
- [01-functions.Rmd](01-introduction/01-functions.Rmd) — One small function
- [01-setup.R](01-introduction/01-setup.R) — Same setup as a script
- [01-r-basics.R](01-introduction/01-r-basics.R) — Longer script of the same steps

## Session 2 — Causation

Datasets come from the `qss` package (`resume`, and `social` for the later GOTV file).

- [02-resume.Rmd](02-causation/02-resume.Rmd) — Callback rates by race. In class.
- [02-subsetting.Rmd](02-causation/02-subsetting.Rmd) — Filters and race by sex. Optional.
- [02-potential-outcomes.R](02-causation/02-potential-outcomes.R) — Script for the potential-outcomes contrast
- [02-social.Rmd](02-causation/02-social.Rmd) — Social-pressure GOTV. Use this in session 16, not session 2.

## Session 3 — One variable

Reads `data/country_indicators.csv` in this folder.

- [03-variable-types.Rmd](03-describing-a-single-variable/03-variable-types.Rmd) — What kind of variable
- [03-summaries.Rmd](03-describing-a-single-variable/03-summaries.Rmd) — Mean, median, sd, IQR
- [03-histograms-boxplots.Rmd](03-describing-a-single-variable/03-histograms-boxplots.Rmd) — Histogram and boxplot
- [03-describe.R](03-describing-a-single-variable/03-describe.R) — Same summaries as a script

## Session 4 — Correlation, part 1

Reads `data/country_indicators.csv` in this folder.

- [04-scatterplots.Rmd](04-correlation-pt1/04-scatterplots.Rmd) — Scatter plots
- [04-correlation.Rmd](04-correlation-pt1/04-correlation.Rmd) — Correlation
- [04-variation.Rmd](04-correlation-pt1/04-variation.Rmd) — Restricted range
- [04-association.R](04-correlation-pt1/04-association.R) — Same association as a script

## Session 5 — Correlation, part 2

Reads `data/country_indicators.csv` in this folder. No new required chapter; same idea as session 4.

- [05-outliers.Rmd](05-correlation-pt2/05-outliers.Rmd) — Outliers
- [05-nonlinear.Rmd](05-correlation-pt2/05-nonlinear.Rmd) — A curve that correlation misses
- [05-ir-examples.Rmd](05-correlation-pt2/05-ir-examples.Rmd) — Several pairs
- [05-regression-preview.Rmd](05-correlation-pt2/05-regression-preview.Rmd) — A first line
- [05-correlation-deep.R](05-correlation-pt2/05-correlation-deep.R) — Same checks as a script

## Session 6 — Regression, part 1

Reads `data/country_indicators.csv` in this folder. Description and prediction, not a cause.

- [06-simple-ols.Rmd](06-regression-description-prediction-pt1/06-simple-ols.Rmd) — One least-squares line
- [06-prediction.Rmd](06-regression-description-prediction-pt1/06-prediction.Rmd) — Fitted values
- [06-democracy.Rmd](06-regression-description-prediction-pt1/06-democracy.Rmd) — A predictor is not a lever
- [06-ols.R](06-regression-description-prediction-pt1/06-ols.R) — Same line as a script

## Session 7 — Regression, part 2

Reads `data/country_indicators.csv` in this folder.

- [07-residuals.Rmd](07-regression-description-prediction-pt2/07-residuals.Rmd) — Residuals
- [07-multiple.Rmd](07-regression-description-prediction-pt2/07-multiple.Rmd) — More than one predictor
- [07-prediction-vs-causation.Rmd](07-regression-description-prediction-pt2/07-prediction-vs-causation.Rmd) — A fitted value is not an effect
- [07-regression-pt2.R](07-regression-description-prediction-pt2/07-regression-pt2.R) — Same steps as a script

## Session 9 — Probability, part 1

Reads `data/survey_attitudes.csv` in this folder.

- [09-frequency.Rmd](09-probability-theory-pt1/09-frequency.Rmd) — Probability as a long-run share
- [09-conditional.Rmd](09-probability-theory-pt1/09-conditional.Rmd) — Conditional probability
- [09-simulate.Rmd](09-probability-theory-pt1/09-simulate.Rmd) — A small simulation

## Session 10 — Probability, part 2

`10-survey-rv.Rmd` reads `data/survey_attitudes.csv`. The other two files simulate coin-toss style draws.

- [10-bernoulli.Rmd](10-probability-theory-pt2/10-bernoulli.Rmd) — One yes-or-no draw
- [10-binomial.Rmd](10-probability-theory-pt2/10-binomial.Rmd) — A count of successes
- [10-survey-rv.Rmd](10-probability-theory-pt2/10-survey-rv.Rmd) — A survey score as a random variable

## Session 11 — Estimation and uncertainty

Reads `data/survey_attitudes.csv` in this folder.

- [11-one-sample.Rmd](11-estimation-and-uncertainty/11-one-sample.Rmd) — One sample
- [11-sampling-dist.Rmd](11-estimation-and-uncertainty/11-sampling-dist.Rmd) — Sampling distribution
- [11-ci.Rmd](11-estimation-and-uncertainty/11-ci.Rmd) — A confidence interval

## Session 12 — Hypothesis testing

Reads `data/survey_attitudes.csv` in this folder.

- [12-two-groups.Rmd](12-hypothesis-testing/12-two-groups.Rmd) — Two groups
- [12-ci-vs-test.Rmd](12-hypothesis-testing/12-ci-vs-test.Rmd) — Interval and test
- [12-fishing.Rmd](12-hypothesis-testing/12-fishing.Rmd) — Too many comparisons

## Session 13 — Reversion to the mean

`13-countries.Rmd` reads `data/country_indicators.csv`. The other two files simulate.

- [13-simulate-reversion.Rmd](13-reversion-to-the-mean/13-simulate-reversion.Rmd) — Simulate reversion
- [13-select-extremes.Rmd](13-reversion-to-the-mean/13-select-extremes.Rmd) — Select the extremes
- [13-countries.Rmd](13-reversion-to-the-mean/13-countries.Rmd) — The same pattern in a country file

## Session 14 — Correlation and causation

Reads `data/country_indicators.csv` and `data/survey_attitudes.csv` in this folder.

- [14-naive-lm.Rmd](14-correlation-and-causation/14-naive-lm.Rmd) — A line that is only an association
- [14-adjust.Rmd](14-correlation-and-causation/14-adjust.Rmd) — Adding GDP does not create a cause
- [14-survey-assoc.Rmd](14-correlation-and-causation/14-survey-assoc.Rmd) — Another association, and a rival story

## Session 16 — Randomized experiments, part 1

Reads `data/diplomacy_experiment.csv` in this folder. The QSS social-pressure file is `02-causation/02-social.Rmd`.

- [16-diplomacy-dim.Rmd](16-randomized-experiments-pt1/16-diplomacy-dim.Rmd) — Difference in means after random assignment

## Session 17 — Randomized experiments, part 2

Reads `data/diplomacy_experiment.csv` in this folder.

- [17-rct-tables.Rmd](17-randomized-experiments-pt2/17-rct-tables.Rmd) — Read a two-group table

## Session 18 — Confounders, part 1

Reads `data/aid_observational.csv` in this folder.

- [18-confounding-intro.Rmd](18-controlling-for-confounders-pt1/18-confounding-intro.Rmd) — A gap that is not yet an effect

## Session 19 — Confounders, part 2

Reads `data/aid_observational.csv` in this folder.

- [19-aid-adjusted.Rmd](19-controlling-for-confounders-pt2/19-aid-adjusted.Rmd) — The same coefficient before and after covariates

## Session 20 — Mechanisms

Reads `data/mechanism_diplomatic_contact.csv` in this folder.

- [20-mechanisms.Rmd](20-mechanisms/20-mechanisms.Rmd) — An effect is not the same size in every subgroup

