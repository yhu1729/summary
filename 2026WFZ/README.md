# 2026WFZ

## ChatGPT (July 2026)

### Summary

The paper proves convergence of entropy-stable split-form continuous summation-by-parts (C-SBP) semi-discretizations for scalar and symmetric hyperbolic conservation laws with homogeneous fluxes. Assuming periodic domains, a smooth exact solution and flux, and globally bounded second flux derivatives, the analysis works directly with the semi-discrete error equation instead of linearization or a projection-based decomposition. Taylor remainders, consistency estimates, and discrete inverse inequalities yield a nonlinear error inequality bounded by a constant-coefficient Riccati initial-value problem. For sufficiently small mesh spacing and degree-$p$ C-SBP operators in $d$ dimensions satisfying $p>1+d/2$, the Riccati envelope remains finite on any fixed finite time interval and vanishes under refinement. This establishes convergence even when the discretization has local linear instabilities. The bound also separates contributions from consistency, flux-Jacobian variation, and discrete gradients, suggesting quantitative criteria for comparing schemes. Extensions to discontinuous SBP methods, state-dependent symmetrizers, nonhomogeneous splittings, and long-time behavior remain open.

### Contributions

1. Proved convergence for entropy-stable split-form C-SBP discretizations of scalar and symmetric hyperbolic systems.
2. Derived the estimate directly from the nonlinear semi-discrete error equation without linearization or projection splitting.
3. Bounded nonlinear error growth by an explicit constant-coefficient Riccati problem.
4. Established the sufficient condition $p>1+d/2$ for finite-time convergence under mesh refinement.
5. Identified how consistency, flux variation, and discrete gradients enter the error-growth coefficients used to compare schemes.
