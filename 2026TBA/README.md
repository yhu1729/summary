# 2026TBA

## Codex/ChatGPT (September 2026)

### Summary

The authors reformulate the electrostatic Vlasov--Ampère system by evolving a conditional distribution in a locally centered and thermal-speed-scaled velocity coordinate. Its density, momentum, and energy moments are fixed, while separate moment equations evolve those physical quantities and use stress and heat flux from the conditional distribution as closures. This division lets positivity controls act on the kinetic equation without corrupting conservation, and concentrates Gauss's law and the quasi-neutral limit in a staggered moment--field subsystem. A slow-manifold reduction removes fast electron time scales from the kinetic equation, and a coupled fixed-point/quasi-Newton solver advances the resulting 1D1V discretization. Tests recover Landau damping and ion-acoustic-shock dynamics while preserving mass, momentum, energy, Gauss's law, and distribution positivity to machine precision. At $\epsilon=10^{-7}$, charge and current scale as $O(\epsilon^2)$ and the electric field agrees with the reduced Ohm's law. The present method is only first-order accurate in space and time and remains explicitly CFL-limited in the kinetic subsystem.

### Contributions

1. Derived an exactly equivalent conditional Vlasov formulation whose first three velocity moments are invariant.
2. Localized conservation laws, Gauss's-law preservation, and quasi-neutral asymptotics in a separate moment--field subsystem.
3. Constructed a staggered finite-difference scheme that simultaneously maintains conservation, positivity, and asymptotic consistency.
4. Demonstrated machine-precision invariants and the expected $O(\epsilon^2)$ quasi-neutral scaling on an ion-acoustic shock.
5. Identified first-order numerical dissipation and the explicit kinetic CFL constraint as the principal limits of the current implementation.
