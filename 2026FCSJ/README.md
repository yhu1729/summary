# 2026FCSJ

## ChatGPT (July 2026)

### Summary

Continuum kinetic solvers can waste most velocity-space degrees of freedom where the particle distribution is negligible. This work introduces nonuniform velocity coordinates into a discontinuous Galerkin full-$f$ gyrokinetic formulation. User-defined mappings concentrate resolution in physically important regions while a continuous intercell representation of the mapping and carefully constructed numerical fluxes preserve the conservative structure. Collisionless dynamics conserve particle number and total energy to machine precision apart from temporal-discretization error; a hybrid polynomial basis also enables the collision operator to conserve particles, momentum, and energy exactly. Tests cover isolated collisionless and collisional behavior and increasingly realistic one-, two-, and three-dimensional Gkeyll simulations of high-temperature-superconducting mirrors, an ASDEX Upgrade scrape-off layer, and LAPD turbulence. The mapped grids reproduce corresponding uniform-grid results using 6--60 times fewer velocity-space cells and achieve 22--60-fold wall-clock speedups. Very coarse grids can nevertheless produce nonphysical negative parallel temperatures, motivating future positivity enforcement and more flexible mappings.

### Contributions

1. Formulated a mapped-coordinate discontinuous Galerkin velocity discretization for full-$f$ gyrokinetics.
2. Designed continuous discrete mappings and numerical fluxes that preserve particles and energy in collisionless dynamics.
3. Introduced a hybrid basis giving the mapped collision operator exact particle, momentum, and energy conservation.
4. Verified accuracy and conservation across collisionless, collisional, and coupled tests in one to three spatial dimensions.
5. Reproduced uniform-grid applications with 6--60 times fewer velocity cells and 22--60-fold speedups.
