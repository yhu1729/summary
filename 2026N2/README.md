# 2026N2

## ChatGPT (July 2026)

### Summary

Third-order edge-based finite-volume schemes traditionally extrapolate physical fluxes from both nodes and average them at an edge midpoint, which complicates reuse of standard Riemann solvers. This note derives an equivalent flux-correction form. The arithmetic mean of extrapolated fluxes is replaced by a general numerical flux evaluated from left and right midpoint states, plus a correction assembled from nodal flux derivatives and reconstructed gradients. Third-order accuracy is retained when the midpoint states are exact for quadratic data; the paper obtains this property with U-MUSCL reconstruction at $\kappa=1/2$. The reformulation lets existing edge-based solvers call unmodified numerical flux functions while adding a compact high-order correction. Manufactured-solution experiments for the three-dimensional Euler equations on irregular tetrahedral grids recover third-order convergence with both HLLC and LDFSS fluxes. The study establishes accuracy rather than application performance; shock robustness and comparative cost in production solvers remain future work.

### Contributions

1. Recast a third-order edge-based discretization into a general numerical-flux plus correction form.
2. Derived the correction without sacrificing the original truncation-error cancellation.
3. Identified quadratic-exact midpoint states as the condition for third-order accuracy.
4. Realized that condition with U-MUSCL reconstruction at $\kappa=1/2$.
5. Verified third-order convergence with HLLC and LDFSS fluxes on irregular tetrahedral grids.
