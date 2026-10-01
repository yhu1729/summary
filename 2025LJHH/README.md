# 2025LJHH

## ChatGPT (July 2026)

### Summary

Explicit Fokker--Planck collision operators impose very small timesteps in collisional gyrokinetic scrape-off-layer simulations. This work implements a Bhatnagar--Gross--Krook (BGK) operator in Gkeyll's discontinuous Galerkin full-$f$ solver, treating collisionless advection explicitly and collisions with backward Euler. A fixed-point correction adjusts the discrete Maxwellian so density, momentum, and energy moments are conserved to near machine precision; the formulation also supports cross-species collisions. Benchmarks against the more detailed Lenard--Bernstein--Dougherty (LBD) operator cover shock relaxation, anisotropic interspecies equilibration, and a two-dimensional axisymmetric ASDEX Upgrade SOL. At converged resolution, BGK and LBD produce similar steady density, temperature, potential, and heat-flux profiles. The BGK scheme is more robust at lower resolution, yielding a net $56\times$ speedup for the SOL case. Its velocity-independent collision frequency cannot reproduce all transport coefficients, cross-species treatment is only partially implicit, and three-dimensional turbulence tests remain future work.

### Contributions

1. Implemented an implicit BGK collision operator for Gkeyll's discontinuous Galerkin gyrokinetic solver.
2. Enforced discrete density, momentum, and energy conservation through iterative Maxwellian correction.
3. Extended the implicit and conservative formulation to cross-species collisions.
4. Validated the operator against LBD results in relaxation tests and an ASDEX Upgrade SOL simulation.
5. Achieved a $56\times$ end-to-end speedup by combining larger timesteps with lower-resolution convergence.
