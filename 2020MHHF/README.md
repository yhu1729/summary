# 2020MHHF

## ChatGPT (July 2026)

### Summary

This work presents an energy-conserving continuum discontinuous Galerkin scheme for the long-wavelength, electromagnetic full-$f$ gyrokinetic system. In a symplectic formulation using parallel velocity, the inductive term $\partial A_\parallel/\partial t$ enters the kinetic equation explicitly; the method computes it directly from a generalized Ohm's law. The phase-space DG discretization conserves particles and, when paired with continuous finite-element field solves so that the discrete Hamiltonian is continuous, conserves energy. Kinetic Alfvén-wave and local kinetic-ballooning-mode benchmarks agree with analytic results and show that the method avoids the Ampère cancellation problem. A nonlinear Gkeyll simulation of helical open field lines, used as a simplified tokamak scrape-off-layer model, provides the first published nonlinear electromagnetic gyrokinetic turbulence calculation on open field lines. Relative to an electrostatic run, it shows less radial transport, shallower density and temperature profiles, and larger, more intermittent density fluctuations. The geometry omits realistic magnetic shear, X-points, gyroaveraging, and a complete positivity treatment, so the nonlinear comparison is demonstrative rather than predictive.

### Contributions

1. Formulated a particle- and energy-conserving DG scheme for electromagnetic full-$f$ gyrokinetics.
2. Derived a direct generalized-Ohm-law update for the inductive parallel electric field.
3. Demonstrated avoidance of the Ampère cancellation problem in two linear electromagnetic benchmarks.
4. Produced the first published nonlinear electromagnetic gyrokinetic turbulence simulation on open field lines.
5. Quantified transport, profile, and intermittency differences between electromagnetic and electrostatic scrape-off-layer simulations.
