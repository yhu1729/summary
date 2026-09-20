# 2025PHR

## ChatGPT (July 2026)

### Summary

Landau-damping code tests often compare only late-time decay rates because reconstructing the early-time response from many complex poles is difficult. This paper derives a semi-analytical time-domain solution of the linearized collisionless Vlasov--Maxwell system that avoids pole summation. Positive- and negative-time frequency-domain solutions are combined using time-reversal symmetry; symmetrizing their spectra removes slow Fourier decay and makes numerical inversion efficient. For the distribution function, a real-axis singularity is subtracted and integrated analytically while the regular remainder is evaluated numerically. The method computes both ion-density and full distribution-function responses to an initial electrostatic density perturbation and extends to arbitrary linear initial conditions by separating symmetric and antisymmetric components. A Langmuir-wave example and comparison with a BSL6D semi-Lagrangian simulation illustrate its use as a high-precision reference and expose velocity-dependent interpolation error. The construction is limited to linearized, collisionless dynamics.

### Contributions

1. Derived a semi-analytical time-domain reference solution for the linearized Vlasov--Maxwell system.
2. Replaced difficult Landau-pole summation with symmetry-conditioned numerical Fourier inversion.
3. Regularized the distribution-function inversion by analytically isolating its real-axis singular contribution.
4. Extended the construction to arbitrary linear initial perturbations through symmetric and antisymmetric decomposition.
5. Demonstrated distribution-level verification of a six-dimensional semi-Lagrangian Vlasov code.
