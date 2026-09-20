# 2025JHJ

## ChatGPT (July 2026)

### Summary

Relativistic continuum-kinetic simulations require a discrete Maxwell--Jüttner equilibrium whose density, bulk velocity, and temperature match prescribed moments. Direct projection onto a finite momentum grid loses distribution tails and perturbs these moments, which can violate conservation in collision operators. The authors derive the required rest-frame moments from the particle four-flux and stress-energy tensor, then develop robust discontinuous Galerkin operations for Lorentz factors and other nonlinear quantities. Computing with spatial four-velocity avoids superluminal intermediate states, while quadrature and weak multiplication or division preserve the modal representation. An iterative Picard correction adjusts the equilibrium's input moments until its discrete moments agree with the targets; density rescaling also avoids fragile evaluation of modified Bessel normalizations. On adequately resolved grids, convergence typically takes 3--20 iterations. A test that otherwise needs about 10,000 momentum cells to reach machine precision uses only 32 corrected cells. In a relativistic BGK relaxation test, density, velocity, and temperature remain conserved near machine precision after ten collision times. The method is applicable beyond DG to other grid-based relativistic kinetic discretizations, but cannot recover distributions whose requested moments are unrealizable on the finite grid.

### Contributions

1. Developed an iterative projection that matches discrete Maxwell--Jüttner density, velocity, and temperature to machine precision.
2. Derived rest-frame equilibrium moments from lab-frame relativistic flux and stress-energy quantities.
3. Constructed robust DG operations for Lorentz factors using four-velocity and physically bounded fallback projections.
4. Quantified finite-grid temperature and momentum limits that determine whether the correction can converge.
5. Demonstrated near-machine-precision conservation in a relativistic BGK relaxation using a practical 32-cell grid.
