# 2026XLDM

## ChatGPT (July 2026)

### Summary

Proton--boron spherical tokamaks combine large ion-mass disparity with neutral-beam-driven toroidal rotation, so centrifugal separation and electrostatic polarization can invalidate single-fluid equilibria. The paper derives a reduced axisymmetric multi-fluid model that retains species-dependent toroidal inertia and a self-consistent electrostatic potential while neglecting poloidal-flow inertia, pressure anisotropy, and finite-orbit-width corrections. Species Bernoulli relations and pointwise quasineutrality close a generalized Grad--Shafranov equation. The accompanying NFEQ solver uses nested Picard and Newton iterations and adjusts the toroidal-field profile to enforce a prescribed plasma current. Fixed-boundary calculations for experimental EHL-2 and reactor-scale EHL-3B recover single-fluid behavior for boron Mach number below about $0.5$. Above unity, boron shifts toward the low-field side; at reactor-relevant high rotation, the density becomes strongly crescent-shaped and the self-consistent potential reaches roughly $10$--$15\,\mathrm{kV}$. The resulting fuel mismatch, pressure redistribution, and altered safety-factor profile show why multi-fluid effects matter for equilibrium targets, although stability, transport, anisotropy, and free-boundary dynamics remain future work.

### Contributions

1. Derived a reduced multi-fluid equilibrium system coupling species-specific Bernoulli distributions, quasineutrality, and a generalized Grad--Shafranov equation.
2. Preserved an elliptic field problem while retaining the dominant centrifugal and electrostatic physics of strongly rotating $p$--$^{11}\mathrm{B}$ plasmas.
3. Developed the NFEQ fixed-boundary algorithm with a pointwise analytic-Jacobian Newton solve, outer Picard iteration, and feedback control of total plasma current.
4. Recovered the static single-fluid limit and identified weak changes for boron Mach number below $0.5$ but substantial separation above unity.
5. Showed that high rotation in EHL-2 and EHL-3B produces low-field-side boron accumulation, multikilovolt potentials, outboard-peaked current, and modified safety-factor profiles.
