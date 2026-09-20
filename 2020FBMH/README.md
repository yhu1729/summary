# 2020FBMH

## ChatGPT (July 2026)

### Summary

The authors construct a conservative discontinuous Galerkin discretization of a gyroaveraged Lenard--Bernstein--Dougherty collision operator for full-$f$, long-wavelength gyrokinetics. The continuous model is an advective--diffusive Fokker--Planck operator that conserves particles, momentum, and energy while satisfying an $H$-theorem. At the discrete level, weak equality supplies consistent primitive moments, while a recovery DG treatment handles velocity-space diffusion. This design preserves the three moments exactly at any resolution, including with piecewise-linear bases when projected quadratic terms are treated carefully. An explicit SSP-RK3 update is accompanied by a conservative stability bound. Implemented in Gkeyll, the operator is tested through relaxation toward a discrete maximum-entropy state, collisional Landau damping, and five-dimensional turbulence in a helical open-field-line model of the Texas Helimak. Low Hermite moments follow analytic relaxation behavior and higher moments converge with resolution. The implementation is limited to like-species collisions; positivity, discrete self-adjointness, a discrete $H$-theorem, and efficient treatment of high collisionality remain future work.

### Contributions

1. Derived a gyroaveraged Dougherty collision operator suitable for full-$f$ long-wavelength gyrokinetic simulations.
2. Introduced a weak-equality and recovery-DG discretization that exactly conserves particles, momentum, and energy.
3. Established practical explicit time-step stability bounds for the combined drag and diffusion operator.
4. Verified relaxation and collisional Landau-damping behavior against analytic moment and dispersion predictions.
5. Integrated the operator into Gkeyll and exercised it in a five-dimensional Texas Helimak turbulence calculation.
