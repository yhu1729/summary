# 2026BCPS

## ChatGPT (July 2026)

### Summary

The authors derive a noncanonical Hamiltonian formulation of the Vlasov-Maxwell system linearized about a Maxwellian distribution and consistent background fields. An energy-Casimir construction yields a quadratic Hamiltonian and Poisson bracket, then a curvilinear transformation makes the model usable in tokamak- and stellarator-like geometries. GEMPIC discretization combines particles for the perturbed distribution with finite-element exterior calculus fields in an exact de Rham sequence, preserving the Hamiltonian structure semidiscretely. A Poisson splitting provides tractable time integrators for Maxwell, coupling, spatial-advection, and Lorentz substeps, implemented in STRUPHY. Weak Landau damping agrees with control-variate and direct-delta-$f$ models at short times, while the geometric method maintains solver-level energy conservation and avoids their long-time noise growth. In magnetized tests it reproduces the analytical Bernstein-wave spectrum, though particle discretization introduces identifiable Case-van Kampen modes at hybrid-frequency harmonics.

### Contributions

1. Derived a quadratic Hamiltonian and noncanonical Poisson structure for Maxwellian-background linearized Vlasov-Maxwell dynamics.
2. Extended the Hamiltonian formulation to curvilinear geometry.
3. Produced a GEMPIC particle-FEEC semidiscretization that preserves geometric constraints.
4. Derived Poisson-split substep integrators and implemented them in STRUPHY.
5. Demonstrated superior long-time Landau-damping stability and recovery of the Bernstein-wave spectrum.
