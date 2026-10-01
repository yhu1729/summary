# 2026NPSB

## ChatGPT (September 2026)

### Summary

Stiff chemical kinetics makes repeated thermochemical time integration costly. AMORE trains one multi-output neural operator to predict temperature and species histories from initial conditions. Its DeepONet variants use either residual networks or a Kolmogorov--Arnold network in the trunk, with a partition-of-unity construction that constrains basis functions. Two gradient-free adaptive losses reweight variables and samples using previous-epoch errors. The authors also compare one-step and two-step training and several ways to enforce species mass-fraction sums, including an invertible map to $n-1$ coordinates and a softmax output. Tests on syngas with 12 states and GRI-Mech 3.0 with 24 active states show improved prediction from adaptive weighting; the Kolmogorov--Arnold trunk yields lower error statistics in the tested cases. Two-step training improves results only marginally while taking longer. Exact unit-sum constraints need adjustment when only a subset of species is modeled.

### Contributions

1. Built a single DeepONet architecture for multiple thermochemical output trajectories.
2. Introduced variable- and sample-adaptive losses requiring no loss-weight gradients.
3. Compared residual-network and Kolmogorov--Arnold trunk designs with partition-of-unity basis functions.
4. Evaluated analytical-coordinate and softmax constructions for exact mass-fraction normalization.
5. Benchmarked single- and two-step training on syngas and GRI-Mech 3.0 kinetics.
