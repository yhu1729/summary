# 2026N3

## Codex/ChatGPT (September 2026)

### Summary

The paper proposes a finite-volume method for hyperbolic conservation-law systems with a strictly convex mathematical entropy and finite propagation speed. At each time step, interface fluxes interpolate between componentwise flux extrema over neighboring-state intervals. Their coefficients are chosen by minimizing the total discrete entropy, translating maximal entropy dissipation into a convex optimization problem. Strict convexity gives a unique updated state when a feasible minimum exists, although the flux coefficients need not be unique; affine constraints can enforce component nonnegativity. The paper establishes a conditional weak-solution result: bounded almost-everywhere convergence of the approximations implies that their limit solves the conservation laws. In one dimension, it presents an entropy-admissibility comparison with bounded-variation solutions constructed by Glimm or wave-front tracking methods. A numerical example for an isentropic Euler system reproduces a rarefaction followed by a shock using an interior-point Newton optimizer. The formulation extends to multiple dimensions, but general convergence is not established, the admissibility comparison is restricted to one dimension, and optimization cost remains a practical limitation.

### Contributions

1. Constructs conservative, consistent finite-volume fluxes by optimizing weights between componentwise flux extrema, minimizing discrete entropy at each time step.
2. Distinguishes uniqueness of the entropy-minimizing state from possible nonuniqueness of its flux weights, and incorporates affine feasibility constraints without losing state uniqueness.
3. Applies the Lax–Wendroff framework to show that a bounded, almost-everywhere convergent sequence of numerical approximations has a weak-solution limit.
4. Presents a one-dimensional comparison with Glimm and wave-front tracking solutions, relating a convergent numerical limit to maximal entropy dissipation on a nontrivial time interval under the stated regularity assumptions.
5. Demonstrates the method on an isentropic Euler Riemann problem with pressure $p(\rho)=\rho^2$, recovering the wave speeds and intermediate state of a rarefaction–shock solution.
