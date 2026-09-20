# 2026G2

## ChatGPT (July 2026)

### Summary

This dissertation studies how state-space computations, including nonlinear recurrent networks, sampling chains, and explicit dynamical solvers, can be parallelized across sequence length. Their recurrences are recast as nonlinear systems and solved with Newton-like iterations whose structured linear subproblems admit parallel associative scans. Quasi-Newton variants reduce state-dimension cost and memory, while trust-region variants use parallel Kalman filtering to improve robustness when undamped iterations fail. The theoretical analysis unifies Newton, Picard, Jacobi, and related fixed-point methods through their Jacobian approximations and derives linear rates governed by approximation error and stability. For nonlinear state-space models, dynamical predictability connects the merit function's conditioning to the largest Lyapunov exponent: stable dynamics can converge in $O(\log T)$ iterations, while unstable dynamics may remain effectively sequential. Experiments on sequence models and sampling problems demonstrate speed, memory, and stability tradeoffs. The results provide both algorithms and a diagnostic for when time parallelism is worthwhile.

### Contributions

1. Developed scan-based quasi-Newton methods with improved state-dimension scaling and memory use.
2. Constructed trust-region parallel Newton methods using parallel Kalman filtering.
3. Unified Newton, Picard, Jacobi, and other fixed-point iterations through Jacobian approximation.
4. Derived convergence rates linking optimization conditioning to dynamical stability.
5. Identified the largest Lyapunov exponent as a criterion for profitable sequence parallelization.
