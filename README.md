# econ3916-lab09-ab-testing
# A/B Testing — Designing the Data-Generating Process

## Objective

I used experimental data and A/B testing methods to estimate treatment effects, measure uncertainty, identify selection bias, and plan appropriate sample sizes.

## Methodology

- I loaded the LaLonde NSW job training experiment with 445 people: 185 trainees and 260 controls.
- I calculated the experimental Average Treatment Effect (ATE).
- I simulated an observational comparison group and separated the observational estimate into the true treatment effect and selection bias.
- I ran a permutation test with 9,999 shuffles.
- I calculated a bootstrap BCa 95% confidence interval for the experimental ATE.
- I conducted a power analysis and estimated the sample sizes needed to detect different earnings effects.
- I analyzed the Cookie Cats A/B test with 90,189 players, comparing gates at levels 30 and 40 using Day-1 retention.
- I wrote and checked `n_needed()` to estimate the sample size required for a new A/B test.

## Key Findings

The trainees earned $1,794.34 more than the randomized control group. The permutation test produced a p-value of 0.0046, and the 95% confidence interval ranged from $575.18 to $3,262.37. In contrast, the simulated observational comparison produced an ATE of −$14,784.45, showing how selection bias can reverse the apparent direction of an effect.

For Cookie Cats, the gate-at-level-30 group had a Day-1 retention rate that was 0.59 percentage points higher than the gate-at-level-40 group. The permutation p-value was 0.0752, so the result was not statistically significant at the 5% level. A new test designed to detect this difference would require 111,193 players per group.
