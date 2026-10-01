# 2026GHDL

## ChatGPT (September 2026)

### Summary

This paper constructs a second-order solver for the six-dimensional Vlasov--Maxwell system by combining Active Flux, operator splitting, and a finite-difference time-domain Maxwell update. Active Flux augments finite-volume cell averages with interface point values, using their compact local evolution to obtain high-order fluxes. Splitting the phase-space transport into one-dimensional advections keeps the stencil and implementation manageable despite the six-dimensional distribution function. The resulting method conserves particle number through its flux formulation and couples charge and current moments to electromagnetic fields. Against the semi-Lagrangian Positive and Flux-Conservative method, the compact Active Flux stencil introduces markedly less numerical dissipation and reduced directional anisotropy. Standard kinetic tests, including Landau damping, two-stream instability, and electromagnetic plasma phenomena, reproduce benchmark behavior at comparable or lower resolution while reducing computational cost. The present discretization does not explicitly enforce higher-moment conservation or positivity in every regime, which the authors identify as targets for further development.

### Contributions

1. Formulated an Active Flux discretization for fully six-dimensional collisionless Vlasov transport.
2. Used operator splitting to reduce the phase-space update to efficient one-dimensional advection solves.
3. Coupled the kinetic update to finite-difference time-domain Maxwell equations.
4. Showed lower dissipation and anisotropy than a semi-Lagrangian positive flux-conservative benchmark.
5. Validated important electrostatic and electromagnetic kinetic phenomena at reduced computational cost.
