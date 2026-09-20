# 2026J

## ChatGPT (July 2026)

### Summary

This paper couples flux-vector splitting with diagonal-norm upwind summation-by-parts (USBP) discontinuous Galerkin operators in physical space, a fast Fourier spectral treatment of the full Boltzmann collision operator, and first-order implicit-explicit time stepping. The semidiscrete formulation is proved locally and globally conservative for mass, momentum, and energy; unlike entropy-stable DG, it does not guarantee entropy decay but avoids costly two-point entropy-stable fluxes. Its fully discrete vanishing-Knudsen limit becomes an explicit flux-split Euler scheme. One-dimensional accuracy, shock propagation, Couette flow, Sod, and Lax tests span continuum through rarefied regimes, including over 85 million degrees of freedom and 50 billion operations per step. Results show high-order accuracy, shock robustness without limiters in most tests, close agreement with DSMC, classical DG, and entropy-stable DG references, and no extra flux-computation overhead.

### Contributions

1. Introduced the first USBP scheme for the nonlinear inhomogeneous full Boltzmann equation using velocity-sign flux splitting.
2. Constructed compatible USBP, quadrature, and dissipation operators and proved discrete conservation of collision invariants.
3. Coupled USBP transport to fast spectral collision evaluation and iteration-free IMEX stepping across Knudsen regimes.
4. Established consistency of the fully discrete kinetic scheme with a flux-split Euler method in the vanishing-Knudsen limit.
5. Demonstrated high-order accuracy, low artificial dissipation, and mostly limiter-free shock stability on five benchmark families.
