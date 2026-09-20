# 2026HTSD

## ChatGPT (July 2026)

### Summary

This paper converts Gaussian Bayesian bolometric tomography into a real-time diagnostic for TCV. Because radiated power over any chosen plasma region is a weighted sum of emissivity pixels, its posterior estimate can be written as a linear combination of bolometer measurements. The expensive coefficients are precomputed from the planned FBT magnetic equilibria, fixed noise and prior hyperparameters, and detector selection; no learned mapping or emissivity-profile training set is required. The method simultaneously estimates total, core, divertor, and main-chamber radiation with Bayesian credible intervals. Tests cover 50 discharges across lower- and upper-single-null, negative-triangularity, X-point-target, and long-legged configurations. Channel selections based on recent failure history yield mean correlations of $0.970$--$0.994$ with offline tomography and region-wise mean RMSEs near $10.5$--$12.6\,\mathrm{kW}$. Excluding several failure-prone channels would have avoided bad data in about $97\%$ of the campaign. Coefficient generation takes roughly $10\,\mathrm{s}$ per equilibrium, comfortably within TCV's inter-discharge interval; integration into feedback control remains future work.

### Contributions

1. Derived real-time regional radiated-power estimators as linear combinations of bolometer signals.
2. Proved equivalence to conventional Gaussian-posterior tomographic estimates under the stated model assumptions.
3. Incorporated discharge-specific magnetic geometry through coefficients precomputed from FBT equilibria.
4. Validated total and regional estimates over 50 discharges spanning five magnetic configurations.
5. Developed and quantified detector-failure strategies suitable for routine real-time deployment.
