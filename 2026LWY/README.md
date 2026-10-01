# 2026LWY

## ChatGPT (September 2026)

### Summary

High-order ideal-magnetohydrodynamics schemes must keep density and pressure positive while maintaining $\nabla\cdot\mathbf{B}=0$. Standard positivity limiters can disrupt continuity of the normal magnetic field. The authors instead construct a globally divergence-free discontinuous Galerkin method that leaves the magnetic field untouched and corrects total energy when needed for admissibility. They add an entropy-Hessian-based convex oscillation-suppression procedure, derive a positivity condition using an optimal convex decomposition, and offer two energy corrections: constrained optimization and closed-form scaling. Conservation is conditional because rare cells where the constraint is infeasible require a fallback energy adjustment. The paper proves positivity under a specified CFL restriction and tests high-order accuracy and robustness on strong shocks, low-$\beta$ plasmas, and other demanding two-dimensional benchmarks. Reported global energy errors are near $10^{-12}$, although strict local energy conservation is lost in fallback cells.

### Contributions

1. Reconciled positivity limiting with globally divergence-free magnetic-field reconstruction.
2. Introduced entropy-Hessian convex oscillation suppression near discontinuities.
3. Developed optimization-based and closed-form energy corrections that are conservative when feasible.
4. Proved positivity under a mild CFL condition from an optimal convex decomposition.
5. Quantified rare fallback events and global energy errors in extreme MHD benchmarks.
