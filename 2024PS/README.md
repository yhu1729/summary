# 2024PS

## ChatGPT (July 2026)

### Summary

This paper proposes a mesh-free collocation solver for path-dependent partial differential equations using signature kernels, universal kernels for sequential data. The PPDE solution is approximated by the minimum-norm element of a signature-kernel reproducing kernel Hilbert space that satisfies the differential equation and boundary data at finitely many paths. For linear PPDEs, the representer theorem reduces this infinite-dimensional optimal-recovery problem to a finite linear system with a unique closed-form solution. The authors establish differentiability and universality properties for the kernel and, under compactness, regularity, uniqueness, and dense-collocation assumptions, prove consistency as the number of collocation points grows. Tests on fractional-Brownian path-dependent heat equations accurately recover analytic conditional expectations. Rough-Bergomi option-pricing experiments obtain errors comparable to Monte Carlo for matched numbers of paths and collocation points. Unlike time-discretized neural PPDE solvers, the method operates on continuous paths, exposes derivatives through kernel differentiation, and solves a convex optimization problem. Error rates versus collocation count and nonlinear PPDE extensions remain open.

### Contributions

1. Formulated PPDE solution as minimum-norm signature-kernel collocation in path space.
2. Reduced linear PPDE recovery to a uniquely solvable finite linear system.
3. Proved kernel regularity, universality, and conditional consistency of the collocation approximation.
4. Recovered analytic fractional-Brownian prices and matched Monte Carlo accuracy in rough-Bergomi tests.
5. Delivered a continuous-path, differentiable, convex alternative to neural and Monte Carlo PPDE solvers.
