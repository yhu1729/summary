# 2026SHJH

## ChatGPT (July 2026)

### Summary

Field-aligned coordinates reduce the resolution needed along magnetic field lines, but their metric becomes singular at a tokamak X-point where the poloidal field vanishes. This paper presents a grid-generation and phase-space discretization method that retains field alignment across both closed core and open scrape-off-layer regions. The tokamak poloidal domain is divided into topologically distinct tracing regions and then into a conforming multiblock grid whose cell corners meet at the X-point. High-accuracy field-line integration directly supplies metric coefficients and geometric quantities. The key numerical choice is to evaluate geometry and surface fluxes only at interior and face quadrature points, never at the singular X-point itself. Implemented in Gkeyll's discontinuous-Galerkin gyrokinetic framework, the method achieves better than first-order convergence for advection, elliptic boundary-value, and geometry tests, although convergence degrades near the X-point. A two-dimensional axisymmetric deuterium simulation in the Spherical Tokamak for Energy Production equilibrium remains well behaved and conserves particles to machine precision. Current grids become coarse near the X-point, and three-dimensional turbulence with parallel-block boundary shifts remains future work.

### Contributions

1. Constructed a conforming field-aligned multiblock grid spanning core and scrape-off-layer regions in X-point geometry.
2. Avoided the coordinate singularity by excluding the X-point from all geometric and numerical-flux evaluations.
3. Derived the gyrokinetic phase-space discretization and required metric quantities for the new grid.
4. Demonstrated better than first-order convergence across advection, boundary-value, and geometry tests.
5. Validated the implementation with a STEP gyrokinetic simulation exhibiting machine-precision particle conservation.
