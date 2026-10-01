# 2026LRBG

## ChatGPT (July 2026)

### Summary

Drift-reduced fluid models remove fast gyrofrequency dynamics from collisional plasma simulations, but common reductions can obscure exact conservation laws. This paper derives a conservative formulation by analytically inverting, without a perturbative truncation, the implicit relation that defines polarization velocity through the time derivative of the electric field. The inversion supplies a transport equation for leading-order perpendicular momentum and closes the reduced fluid system in arbitrary magnetic geometry. Electromagnetic fluctuations are retained rather than imposing the electrostatic limit. Starting from the species equations and Maxwell equations, the authors establish exact conservation of mass, charge, energy, and the relevant momentum components, including exchanges between particles and fields. The construction is independent of the chosen fluid closure and can therefore be combined with Braginskii two-fluid or more general multispecies closures. Unlike variational reductions based on an expanded guiding-center Lagrangian, the method operates directly on the fluid equations and makes exact conservation the organizing constraint. Its implications for long-time plasma-turbulence calculations and conservative numerical solvers remain to be assessed computationally.

### Contributions

1. Analytically inverted the implicit polarization-velocity relation without a perturbative expansion.
2. Derived a closed conservative drift-reduced system in arbitrary magnetic geometry.
3. Retained electromagnetic fluctuations beyond the electrostatic approximation.
4. Proved exact mass, charge, energy, and momentum conservation for the reduced equations.
5. Made the formulation independent of the fluid closure, enabling two-fluid and multispecies applications.
