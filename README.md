# Landing Page A/B Testing Analysis

Business-focused A/B testing case study evaluating whether a new landing page improves user conversion. The analysis validates experiment quality, measures the impact on conversion, and translates statistical findings into a product recommendation.

## Business Problem

An e-commerce company introduced a new landing page to increase customer conversion. Rather than deploying the new design to every user, an A/B experiment was conducted to compare its performance against the existing landing page.

This project analyzes the experiment to determine whether the observed change in conversion is large enough to support a product rollout.

## Business Question

**Should the company replace the existing landing page with the new landing page?**

## At a Glance

| Metric | Value |
|---------|-------|
| Dataset | E-commerce A/B Testing Dataset |
| Users Collected | 294,478 |
| Users Analyzed | 290,584 |
| Invalid Records Removed | 3,894 |
| Experiment Groups | Control and Treatment |
| Primary Metric | Conversion Rate |
| Statistical Test | Two-Proportion Z-Test |
| Confidence Level | 95% |
| Final Decision | Retain Existing Landing Page |

## Dataset

| Attribute | Value |
|----------|-------|
| Source | Kaggle |
| Dataset | E-commerce A/B Testing |
| Records Collected | 294,478 |
| Records Used | 290,584 |
| Files | `ab_test.csv`, `countries_ab.csv` |
| Link | [Dataset](https://www.kaggle.com/datasets/ahmedmohameddawoud/ecommerce-ab-testing) |

The dataset contains user-level experiment data including experiment group assignment, landing page shown, and conversion outcome. It is based on the well-known Udacity A/B Testing project and is commonly used to study online experimentation. :contentReference[oaicite:1]{index=1}

## Analysis Workflow

| Stage | Business Objective |
|---------|-------------------|
| Experiment Validation | Verified experiment quality by identifying duplicate users and incorrect page assignments before analysis. |
| Data Cleaning | Removed **3,894** invalid records to ensure every user contributed only one valid observation. |
| Experiment Overview | Evaluated traffic allocation and established the baseline conversion rate across **290,584** users. |
| Conversion Analysis | Compared conversion performance between the control and treatment landing pages. |
| Statistical Validation | Tested whether the observed conversion difference was statistically significant using a Two-Proportion Z-Test and a 95% confidence interval. |
| Business Recommendation | Converted statistical findings into a product decision supported by data. |

## Experiment Results

| Metric | Result |
|---------|--------|
| Overall Conversion Rate | **11.96%** |
| Control Conversion Rate | **12.04%** |
| Treatment Conversion Rate | **11.88%** |
| Absolute Difference | **-0.16 Percentage Points** |
| P-value | **0.1899** |
| 95% Confidence Interval | **-0.39% to 0.08%** |

## Key Business Insights

- The experiment initially contained **294,478** user records, of which **3,894** invalid observations were removed before analysis to improve experiment reliability.
- The final analysis included **290,584** unique users, providing a large sample for comparing conversion performance.
- Traffic allocation remained almost perfectly balanced, with **50.01%** of users assigned to the treatment group and **49.99%** assigned to the control group.
- The new landing page achieved a conversion rate of **11.88%**, compared with **12.04%** for the existing landing page.
- The observed difference of **-0.16 percentage points** was not statistically significant (**p = 0.1899**).
- The **95% confidence interval (-0.39% to 0.08%)** includes zero, indicating that the true impact of the new landing page could be slightly negative, slightly positive, or negligible.

## Business Recommendation

The analysis does not provide sufficient statistical evidence that the new landing page improves user conversion.

Based on the experiment results, replacing the existing landing page would introduce implementation effort without demonstrating a measurable improvement in business performance.

The recommended decision is to retain the existing landing page and evaluate an improved design through a future A/B experiment.

## Skills Demonstrated

`A/B Testing` `Product Analytics` `Experiment Design` `Statistical Hypothesis Testing` `Confidence Intervals` `Data Validation` `Data Cleaning` `Exploratory Data Analysis` `Business Analytics` `Business Decision Making` `Python` `Pandas` `NumPy` `Matplotlib` `Statsmodels`

## Repository Structure

```text
landing-page-ab-testing-analysis/

├── landing_page_ab_testing.ipynb
├── README.md
├── requirements.txt
└── data/
    └──  ab_test.csv
```

## Future Improvements

- Analyze experiment performance across user segments such as country.
- Evaluate Sample Ratio Mismatch (SRM) as an additional experiment quality check.
- Estimate the business impact under different traffic and conversion scenarios.
- Build an interactive dashboard to monitor experiment performance and key metrics.

## Author

[**Anurag Chauhan**](https://www.linkedin.com/in/theanuragchauhan/)
