This tutorial provides a step-by-step guide for generating CDC anthropometric z-scores, percentiles, and related metrics for weight, height, and body mass index (BMI) in R. It focuses on calculating accurate BMI z-scores for children and adolescents **aged 24 to 240.5 months** using the 2000 CDC growth charts (Kuczmarski et al., 2002).

The primary R package used is `cdcanthro`, which is recommended by the CDC on their [Growth Chart Training website](https://www.cdc.gov/growth-chart-training/hcp/computer-programs/r-programs.html). A critical update in 2022 changed how the CDC calculates BMI z-scores and percentiles for children with obesity by introducing extended BMI metrics. These new metrics differ from those produced by earlier software versions.

**The `cdcanthro` package implements this update by generating a seamless BMI z-score (bmiz) that uses:**

-   The standard LMS method (Cole & Green, 1992) for children with a BMI < 95th percentile.
-   The new extended BMI method (CDC, 2022) for children with a BMI ≥ 95th percentile, allowing for more precise tracking of severe obesity.


