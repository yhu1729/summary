# 2026CMPT

## ChatGPT (July 2026)

### Summary

Caplan et al. develop a Lagrangian particle method for the spherical shallow-water equations in which particles are represented by weighted spherical Voronoi, or power, cells. A halfspace-clipping construction and spherical-quadtree neighbor search make the tessellation practical at very large scale. Cell geometry supplies discrete gradient and divergence operators, a semi-implicit update relaxes the gravity-wave time-step restriction, and semi-discrete optimal transport adjusts cell weights to enforce each particle's target mass. Williamson and Galewsky benchmarks show approximately first-order convergence, momentum and energy behavior comparable to a recent Lagrangian solver, and broadly consistent height fields relative to an Eulerian TRiSK solver. The method avoids polar singularities by working in three-dimensional Cartesian coordinates, but its current linear solves and repeated optimal-transport iterations make it 12--20 times slower than the comparison solver, and some test solutions remain noticeably smoothed.

### Contributions

1. Introduced a power-cell Lagrangian discretization of the spherical shallow-water equations.
2. Developed spherical halfspace-clipping and quadtree algorithms that compute a 100-million-site Voronoi diagram in under two minutes.
3. Combined power-cell differential operators with semi-implicit time integration without artificial viscosity or particle merging.
4. Enforced local particle mass through a Newton solution of a semi-discrete optimal-transport problem.
5. Validated four standard spherical-flow benchmarks and quantified accuracy, conservation, and runtime against an Eulerian solver.
