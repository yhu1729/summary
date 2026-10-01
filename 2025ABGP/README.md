# 2025ABGP

## ChatGPT (July 2026)

### Summary

High-order discontinuous Galerkin approximations on polytopic meshes can overshoot physical solution bounds. The paper constructs an arbitrary-order composite method for second-order elliptic problems that enforces prescribed bounds at user-selected points inside each polytope. Starting from an interior-penalty DG discretization, it introduces a local simplicial submesh, projects recovered values onto a convex nodal constraint set, and stabilizes the projection's kernel through a nonlinear term. Submesh nodes may be quadrature points, yet the global unknown count remains unchanged. The DG penalty depends only on the coarse polytopic mesh, not submesh granularity, and the formulation reduces to the baseline DG method where no bound is violated. Strong monotonicity and the Browder--Minty theorem establish existence and uniqueness. Because standard interpolants do not meet these constraints, the authors construct a specialized bound-preserving interpolant and derive optimal a priori estimates for sufficiently smooth solutions. A matrix formulation permits reuse of existing DG operators, while a semismooth Newton iteration solves the nonlinear system. Tests with degree-one through degree-three elements recover optimal rates and remove overshoots and undershoots around boundary and interior layers over strongly varying diffusion parameters. The guarantee is nodal at chosen points, not a pointwise bound everywhere.

### Contributions

1. Developed an arbitrary-order nodally bound-preserving DG method for second-order elliptic problems on general polytopic meshes.
2. Allowed bounds to be enforced at freely selected submesh nodes without adding global degrees of freedom or changing the coarse-mesh penalty parameter.
3. Designed a projection-kernel stabilization with the monotonicity needed to prove existence and uniqueness.
4. Constructed a nonstandard bound-preserving interpolant and obtained optimal a priori error estimates for smooth solutions.
5. Demonstrated optimal convergence and suppression of nonphysical oscillations for smooth, boundary-layer, and interior-layer problems.
