# 2026SDLM

## ChatGPT (July 2026)

### Summary

Variable-density shallow-water flow coupled to solute transport must preserve hydrostatic equilibria while keeping water depth and concentration nonnegative. This paper reformulates the coupled system with auxiliary variables that expose a still-water equilibrium even when bottom topography and mixture density vary. A discontinuous Galerkin discretization with Lax--Friedrichs fluxes is designed to preserve that equilibrium exactly for the specified auxiliary-variable choices. The authors derive sufficient positivity conditions for cell averages and add a scaling limiter that enforces nonnegative depth and concentration without destroying high-order accuracy or the well-balanced state. One- and two-dimensional tests verify the designed convergence order, preservation of stationary solutions, wet/dry robustness, and consistent transport of constant concentration through rapidly changing flows. The present two-dimensional implementation uses structured grids and therefore targets simple domains; extension to unstructured meshes and complex geometries is deferred.

### Contributions

1. Formulated coupled variable-density shallow-water and solute equations with equilibrium-compatible auxiliary variables.
2. Constructed a discontinuous Galerkin scheme that exactly preserves the targeted still-water state.
3. Proved sufficient conditions for nonnegative water depth and solute concentration.
4. Added a positivity limiter compatible with high-order accuracy and well-balancedness.
5. Verified accuracy, equilibrium preservation, wet/dry behavior, and transport consistency numerically.
