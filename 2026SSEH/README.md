# 2026SSEH

## Claude (September 2026)

### Summary

The authors study adaptive sparse-grid discontinuous Galerkin (DG) discretizations of the Bhatnagar–Gross–Krook (BGK) kinetic model in four- and six-dimensional phase space, where full-grid DG is impractical. The distribution is expanded in Alpert multiwavelets, and coefficient decay across levels drives simultaneous refinement and coarsening of an ancestor-complete grid after each step of an implicit-explicit Runge–Kutta scheme with explicit upwind advection and implicit relaxation. Interpolating the nonseparable Maxwellian directly on the sparse grid violates the collision invariants when velocity resolution is coarse, so they introduce a hybrid interpolation: interpolation in position only, with exact error-function velocity projections that exploit velocity separability. They prove that it reproduces density, momentum, and energy for polynomial degree $k\ge2$. Tests comprise a 3x3v relaxation problem, a radial 2x2v Sod problem at Knudsen numbers 0.001, 0.1, and 1, a shear flow, and expansion problems from dynamical low-rank studies. In the relaxation test with $k\ge2$, the hybrid Maxwellian conserves moments to roundoff, whereas phase-space interpolation errs by 0.1–9%; fluid-regime results match Euler references; rarefied velocity distributions depart from the Chapman–Enskog perturbation; and active degrees of freedom shrink by factors from about three to over five thousand relative to full grids. All computations use the ASGarD library.

### Contributions

1. Introduced a hybrid Maxwellian interpolation and proved that it preserves the discrete BGK collision invariants on ancestor-complete adaptive sparse grids for $k\ge2$.
2. Assembled an adaptive sparse-grid DG–IMEX algorithm for BGK that refines and coarsens in one pass, keeps grids ancestor complete, and adds nonlinear refinement driven by the interpolated Maxwellian.
3. Demonstrated that a phase-space-interpolated Maxwellian causes conservation errors and oscillations that densify the grid, whereas the hybrid version needs orders of magnitude fewer degrees of freedom in the shear-flow test.
4. Resolved sharp gradients first in position and then in velocity for a radial Sod problem from fluid to transitional regimes, showing kinetic perturbations differing from the Navier–Stokes correction by nearly a factor of four at $\nu=1$, where that correction also turns negative.
5. Showed on low-rank benchmarks that sparse grids compress distributions whose rank keeps growing, with phase-space degrees of freedom decreasing after an initial rise, and ran 3x3v cases with about 0.12% of the full-grid degrees of freedom.
