# 2026ZW

## ChatGPT (September 2026)

### Summary

High-order implicit finite volume methods can produce negative density or pressure while iteratively solving the compressible-flow equations. This paper develops a positivity-preserving procedure for dual-time stepping on unstructured grids. A physical-time-step limit uses the current residual to estimate the next cell average and constrains that estimate with a lower bound that accounts for estimation error. During the inner nonlinear solve, pseudo-time-step limiting and a correction to the computed increment keep intermediate cell averages admissible. A scaling limiter then makes reconstruction polynomials admissible without changing their cell averages. The authors analyze why the procedure retains high-order accuracy and test it with fourth-order spatial reconstruction and implicit time integration on inviscid and viscous benchmarks. The reported tests show robust, well-resolved solutions; admissibility is enforced during the iterations rather than checked only after convergence.

### Contributions

1. Introduced physical-time-step limiting to ensure an admissible next-time-level cell average.
2. Combined pseudo-time-step limiting with increment correction for positivity during inner iterations.
3. Coupled cell-average protection to polynomial scaling for positive reconstructed states.
4. Analyzed the method's accuracy preservation and dependence on limiting parameters.
5. Demonstrated the approach on high-order unstructured-grid compressible-flow benchmarks.
