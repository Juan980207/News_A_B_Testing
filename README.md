# A/B Testing on Online News Popularity

This project applies a complete A/B testing workflow on the [Online News Popularity dataset](https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity) to test whether certain characteristics of a news article (such as title length) affect its likelihood of becoming popular.

## Objective

The goal is to determine whether **Group B** (<=8 Images included in the article) leads to a **significantly higher popularity metric** compared to **Group A** (>8 Images Included in the article). Popularity is measured as the number of shares an article receives.

## Methodology

- **Data Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity)
- **A/B Group Definition**: Based on one chosen feature (Images).
- **Metric**: Number of shares.
- **Statistical Tests Used**:
  - Shapiro-Wilk (normality)
  - Levene's test (homogeneity of variances)
  - Welch's t-test or Mann-Whitney U (depending on assumptions)
- **Effect Size Measures**:
  - Cohen's d
  - Rank Biserial Correlation (RBC)
  - Common Language Effect Size (CLES)

## Key Findings
- The difference between groups was **statistically significant** with a p-value < 0.001.
- However, the **effect size was small**, suggesting the practical impact may be limited.
- Visualizations confirmed distribution skew and variance differences → robust testing was used.
