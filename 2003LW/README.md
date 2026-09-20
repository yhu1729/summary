# 2003LW

## ChatGPT (July 2026)

### Summary

Eight explicit finite-difference schemes for the compressible Euler equations are compared across demanding one- and two-dimensional tests. The selection spans central and upwind-biased methods, dimensional splitting, Riemann solvers, flux limiting, hybridization, and Runge--Kutta time stepping; every scheme is at least formally second-order accurate. Seven one-dimensional Riemann problems and the Woodward--Colella blast-wave problem permit quantitative comparisons, including relative $L^1$ errors, while the two-dimensional suite probes smooth-flow accuracy, interacting Riemann waves, strong shocks, unstable interfaces, symmetry preservation, odd--even decoupling, and vortex advection. Smooth periodic tests recover the superior formal accuracy of WENO and PPM, but discontinuous and multidimensional problems expose method-dependent trade-offs in dissipation, shock and contact resolution, oscillations, grid-aligned artifacts, and symmetry errors. CPU timings are reported but treated cautiously because the implementations required different adaptations to a common framework. No scheme is uniformly best: rankings change with the flow and diagnostic. The work therefore supplies a comparative benchmark rather than a universal recommendation, with complete results and animations provided separately.

### Contributions

1. Compared eight representative high-resolution finite-difference schemes within one computational framework.
2. Assembled a broad benchmark suite spanning exact-solution Riemann tests and difficult multidimensional flows.
3. Quantified one-dimensional errors and smooth-problem convergence while also reporting implementation-qualified timing data.
4. Documented scheme-specific failures, including excessive diffusion, oscillations, symmetry loss, grid alignment, and odd--even decoupling.
5. Established that method quality is problem-dependent and released a larger body of results for continued code assessment.
