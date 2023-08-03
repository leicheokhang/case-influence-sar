# Case influence analysis for Bayesian SAR models

This repo contains the raw and tidy output for the Monte Carlo study and the crime data set.

## Monte Carlo study

| Parameter | Description |
| --------- | ----------- |
| Replication | Each simulation contains `K = 100` replications. |
| Weighting matrix | Two weighting matrices are considered. `W = W1` denotes the one-ahead-one-behind circular weighting matrix and, `W = W2` denotes the two-ahead-two-behind circular weighting matrix. |
| Sample size | At each replication of the simulation, we generate a sample based on the prespecified parameters, with the sample size set to `N = 50, 100, 150`. |
| Autoregressive parameter | We consider `rho = 0.3, 0.6, 0.9`, representing weak, moderate and strong spatial dependence, respectively. |
| Degree of distortion | We consider `delta = 0, 1, 2, 3, 4, 5, 6`. When `delta = 0`, there is no outlier. Estimated percentiles of the largest component in the case influence diagnostic are computed. The results determine the threshold values to identify influential observations. When `delta = 1, 2, 3, 4, 5, 6`, the `42`nd observation `y_otlr` is selected and replaced by the value `y_otlr + delta`. Outlier detection rate is computed. |
