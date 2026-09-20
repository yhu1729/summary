# 2026ODDE

## ChatGPT (July 2026)

### Summary

STORM models three-dimensional turbulence and filament dynamics across a tokamak scrape-off layer, where turbulent transport controls plasma exhaust loads on material surfaces. It solves a drift-reduced, cold-ion, collisional fluid system in BOUT++ using a flux-surface-aligned grid, mostly finite differences, and field-aligned parallel derivatives. Parallel fluxes are placed on a staggered grid to suppress checkerboard modes, while a fully implicit, matrix-free CVODE integrator accommodates fast electron thermal conduction. The paper provides a consolidated specification of the plasma equations, Boussinesq options, sheath and radial boundary conditions, elliptic inversions, initialization procedures, sources, and synthetic probe diagnostics. It also documents BOUT++ version-4 improvements developed for STORM: geometric quantities can be represented consistently at cell faces, parallel transforms account for field location, and field-aligned derivative machinery supports wider stencils. These changes remove a prior staggered-geometry inconsistency that could restrict spatial convergence. The implementation supports turbulence and seeded-filament studies in slab and realistic tokamak geometries, but its collisional closure limits use in low-collisionality regimes, and electromagnetic operation in tokamak geometry remains unresolved.

### Contributions

1. Presented a complete, reproducible specification of the three-dimensional STORM scrape-off-layer turbulence model and its BOUT++ implementation.
2. Established a staggered parallel-grid discretization that suppresses grid-scale checkerboard instabilities in the fastest plasma dynamics.
3. Upgraded BOUT++ geometry and parallel-transform infrastructure so staggered variables use consistent cell-face metrics and field-aligned derivatives.
4. Integrated practical numerical components for full simulations, including elliptic solvers, implicit CVODE time integration, sheath and radial boundaries, initialization, and source models.
5. Added simulation-facing diagnostics and workflows for both statistically steady turbulence and seeded filaments, including high-frequency synthetic Langmuir-probe output.
