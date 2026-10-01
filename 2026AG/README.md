# 2026AG

## ChatGPT (July 2026)

### Summary

This paper establishes finite-element error estimates for second-order hyperbolic equations whose material coefficients vary in both space and time, including the sign-changing gain/loss term induced by temporal modulation. The central device is a time-dependent Ritz-like projection that incorporates this first-order term and permits control of the projection error and its time derivatives. Combined with a duality argument and energy estimates, it yields the optimal semidiscrete bound $\|u-U_h\|_{L^\infty(0,T;H^1)}\leq Ch^{r-1}$ for conforming polynomial spaces under stated regularity assumptions. One-dimensional experiments with mass-lumped quadratic elements and leapfrog or leapfrog--Crank--Nicolson time stepping recover second-order $H^1$ and third-order $L^2$ convergence for smooth time-modulated density, bulk modulus, and gain/loss coefficients. A final high-contrast example models 50 time-modulated subwavelength resonators and exhibits strong, spatially localized, exponentially growing wave amplification. Thus, the work both closes a convergence-theory gap for non-autonomous wave operators and demonstrates behavior relevant to actively modulated metamaterials.

### Contributions

1. Formulated a finite-element convergence framework for wave equations with fully space-time-dependent coefficients and gain/loss terms.
2. Introduced a time-dependent Ritz-like projection adapted to amplification and attenuation in the medium.
3. Proved optimal $H^1$ convergence for the semidiscrete Galerkin approximation and bounds for projection time derivatives.
4. Numerically confirmed the predicted $H^1$ and $L^2$ rates with mass-lumped quadratic finite elements.
5. Demonstrated localized exponential field growth in a chain of time-modulated subwavelength resonators.
