# Landing Page A/B Testing Analysis

## Overview

An e commerce company introduced a new landing page to improve user conversion. An A/B test was conducted to compare the new page with the existing page before making a decision.

This project evaluates the experiment data to determine whether the new landing page delivered a meaningful improvement in conversion.

## Business Question

**Does the new landing page improve conversion compared with the existing landing page?**

## Dataset

The dataset contains user level experiment data with information about:

| Field            | Description                |
| ---------------- | -------------------------- |
| User ID          | Identifier for each user   |
| Experiment Group | Control or Treatment       |
| Landing Page     | Page shown to the user     |
| Converted        | Whether the user converted |
| Time             | Experiment timestamp       |

The dataset initially contained **294,478 records**.

## Analysis Approach

The analysis followed four main steps:

1. Validate the experiment data and identify data quality issues
2. Compare conversion rates between the two groups
3. Test whether the observed difference was statistically significant
4. Translate the results into a business recommendation

## Data Validation

Before comparing conversion, the experiment data was checked for duplicate users and incorrect group and page assignments.

The analysis found:

**3,894 duplicate user records**

**3,893 records with inconsistent experiment group and landing page assignments**

Incorrect assignments were removed first, followed by duplicate user removal.

The final dataset contained **290,584 unique users**.

The experiment groups were also well balanced:

| Group     |   Users |  Share |
| --------- | ------: | -----: |
| Control   | 145,274 | 49.99% |
| Treatment | 145,310 | 50.01% |

## Conversion Results

Conversion rate was used as the primary measure of landing page performance.

**Conversion Rate = Converted Users ÷ Total Users**

| Metric          | Existing Page |   New Page |
| --------------- | ------------: | ---------: |
| Users           |       145,274 |    145,310 |
| Converted Users |        17,489 |     17,264 |
| Conversion Rate |    **12.04%** | **11.88%** |

The new page had a **0.16 percentage point lower** conversion rate than the existing page.

However, this observed difference alone does not establish that the two pages perform differently. Statistical testing was used to determine whether the difference was meaningful.

## Statistical Analysis

A **Two Proportion Z Test** was used to compare the conversion rates of the two groups.

The test evaluated whether the difference between the existing and new landing pages was statistically significant at a **5% significance level**.

| Measure                  |                       Result |
| ------------------------ | ---------------------------: |
| Existing Page Conversion |                       12.04% |
| New Page Conversion      |                       11.88% |
| Difference               | 0.16 percentage points lower |
| Z Statistic              |                       1.3109 |
| P Value                  |                   **0.1899** |
| 95% Confidence Interval  |      **−0.3938% to 0.0781%** |

The p value of **0.1899** is greater than the 0.05 significance level.

The confidence interval also includes zero.

Therefore, the experiment does not provide sufficient statistical evidence that the new landing page changes conversion.

## Key Insights

The existing page achieved a **12.04% conversion rate**, while the new page achieved **11.88%**.

The new page therefore performed slightly worse in the observed experiment, with a difference of **0.16 percentage points**.

However, the difference was **not statistically significant**, meaning the observed gap could reasonably be due to variation in the experiment.

## Recommendation

### Retain the Existing Landing Page

Based on the experiment results, the **existing landing page should be retained**.

The new page did not demonstrate a statistically significant improvement in conversion, so the available evidence does not support replacing the existing page.

## Tools and Methods

| Category                | Details                                                                              |
| ----------------------- | ------------------------------------------------------------------------------------ |
| **Programming**         | Python                                                                               |
| **Libraries**           | Pandas, NumPy, Matplotlib, Statsmodels                                               |
| **Analysis**            | Data Cleaning, Experiment Validation, Conversion Analysis                            |
| **Statistical Methods** | A/B Testing, Two Proportion Z Test, Hypothesis Testing, Confidence Interval Analysis |



Project by [**Anurag Chauhan**](https://www.linkedin.com/in/theanuragchauhan/)
