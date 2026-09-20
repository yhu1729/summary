# 2026FUSJ

## Codex/ChatGPT (September 2026)

### Summary

GENE-X is extended from axisymmetric tokamaks to non-axisymmetric stellarators while retaining its full-$f$ gyrokinetic model, which evolves the complete particle distribution. The flux-coordinate independent approach uses local field-line tracing between poloidal grids and remains usable across magnetic islands and the scrape-off layer, where field lines intersect material boundaries. Analytic Dommaschk vacuum fields, plane-dependent geometry and meshes, and masked array operations remove axisymmetry assumptions in GENE-X and its shared PARALLAX infrastructure. Manufactured-solution tests recover second-order convergence of the distribution function and electromagnetic fields in three-dimensional geometry. A source-free, low-pressure simulation covers the magnetic axis through a non-segmented island divertor. It develops large edge fluctuations, gradient-localized turbulent transport, and a radial electric-field well. Comparable perpendicular ion and electron heat input to the scrape-off layer, combined with weaker parallel ion losses, explains ion-temperature accumulation there. This is a proof of capability rather than experimental validation: the calculation uses vacuum geometry, simplified Dirichlet wall conditions, one stellarator field period, and long-wavelength and small-field-pitch approximations.

### Contributions

1. Enabled global Eulerian gyrokinetic simulations spanning the stellarator core, edge, and island-divertor scrape-off layer within one tokamak/stellarator codebase.
2. Implemented and verified analytic three-dimensional vacuum magnetic fields and an approximate flux-surface label for mesh construction, initialization, and diagnostics.
3. Generalized PARALLAX and GENE-X data structures to plane-dependent meshes, field-line maps, and elliptic solvers, with masks distinguishing active, boundary, and filler points.
4. Verified second-order convergence in three-dimensional geometry by refining space, velocity space, and time in manufactured-solution tests, while retaining axisymmetric verification results.
5. Demonstrated self-consistent edge turbulence and related scrape-off-layer ion heating to the imbalance between cross-field heat supply and species-dependent parallel exhaust.
