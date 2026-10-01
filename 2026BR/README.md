# 2026BR

## ChatGPT (September 2026)

### Summary

This paper extends compact Runge--Kutta flux reconstruction (cRKFR) to hyperbolic systems with stiff source terms and non-conservative products, which cannot generally be expressed as flux divergences. An implicit--explicit time discretization treats source terms implicitly at each solution point while keeping advection explicit and requiring only one inter-element numerical flux evaluation per time step. Interface fluxes represent non-conservative terms; a first-order finite-volume method on element subcells is blended with the high-order method near nonsmooth solutions. Flux and subcell limiters enforce physical admissibility, such as positive density and pressure, under the paper's assumptions on the low-order scheme and admissible set. Tests cover stiff scalar equations, reactive Euler flow, the ten-moment model, shear shallow water flow, GLM magnetohydrodynamics, and multi-ion magnetohydrodynamics. Smooth-wave and manufactured-solution tests recover the expected accuracy, while shock and instability tests show robust behavior. The authors identify path-conservative and well-balanced extensions as open work.

### Contributions

1. Extended the time-averaged cRKFR formulation to stiff sources through point-local implicit--explicit Runge--Kutta updates.
2. Formulated interface numerical fluxes for non-conservative products while retaining one inter-element flux computation per time step.
3. Built a first-order subcell finite-volume scheme and blended it with high-order cRKFR for nonsmooth solutions.
4. Combined interface flux limiting and additional subcell blending to preserve admissibility at solution points under stated assumptions.
5. Verified accuracy and robustness across stiff reactive, shallow-water, single-ion MHD, and multi-ion MHD tests.
