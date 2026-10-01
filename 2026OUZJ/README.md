# 2026OUZJ

## ChatGPT (July 2026)

### Summary

The full-$f$, electromagnetic, collisional gyrokinetic code GENE-X is coupled to a one-moment fluid-neutral model for edge and scrape-off-layer studies. The neutral density evolves through a diffusion--advection equation, with charge exchange represented diffusively and neutral velocity and temperature prescribed from ion moments. For electrons, ions, and atomic neutrals, the work derives Krook-like ionization and three-body-recombination operators, maps them heuristically into gyrocenter coordinates, and uses AMJUEL reaction and cooling rates. Mixing parameters enforce conservation of mass, nuclei, free-plus-bound electrons, momentum, and kinetic energy in the conservative operator; a separate electron term accounts for binding-energy and radiative losses without changing density or momentum. Velocity-space refinement shows at least fourth-order convergence and near-machine-precision conservation, limited chiefly by parallel-velocity quadrature. Relaxation tests show that atomic reactions cool electrons, alter densities, and accelerate isotropization relative to Coulomb collisions alone. In a divertor-like case, newly ionized cold, slow particles create skewed, non-Maxwellian distributions and conductive heat fluxes comparable to standard fluid estimates. The tests establish implementation consistency but stop short of nonlinear turbulence validation, which remains necessary for assessing macroscopic transport effects.

### Contributions

1. Added a tightly coupled gyrokinetic-plasma/fluid-neutral framework to GENE-X.
2. Constructed gyrocenter Krook-like operators for ionization and recombination in a three-species hydrogenic system.
3. Enforced particle, momentum, and conservative-energy constraints while separately representing atomic binding and radiative losses.
4. Verified the implemented conservation laws through velocity-space convergence to near machine precision.
5. Demonstrated neutrals-driven isotropization, non-Maxwellian distortion, skewness, and heat flux in relaxation tests.
