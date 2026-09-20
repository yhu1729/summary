# 2025VKC

## ChatGPT (July 2026)

### Summary

Vandecasteele, Karris, Cloninger, and Kevrekidis extend matrix-free timestepper methods for steady states from deterministic systems to stochastic particle simulations. Instead of treating a stochastic timestepper as a map on individual particle realizations, the paper reformulates it as an operator on probability measures using optimal transport. This allows steady states to be computed through smooth distributional representations, including cumulative- and inverse-cumulative-distribution-function timesteppers in one dimension and CDF-related or sliced-Wasserstein representations in higher dimensions. The authors analyze why naive particle-level Newton--Krylov finite differences fail under stochastic noise: Jacobian-vector estimates acquire a noise-dependent bias-variance tradeoff scaling with the perturbation size. Smooth distributional timesteppers reduce microscopic variability and restore robust Newton--Krylov convergence. Numerical examples recover steady-state distributions in noisy particle systems and clarify that representation smoothness is the key condition for fast matrix-free solvers.

### Contributions

1. Recast stochastic particle timesteppers as operators on probability measures.
2. Connected steady-state computation with optimal-transport residual formulations.
3. Analyzed stochastic noise in finite-difference Jacobian-vector products.
4. Introduced smooth ICDF, CDF, and sliced-Wasserstein timestepper representations.
5. Demonstrated Newton--Krylov steady-state computation for noisy particle distributions.
