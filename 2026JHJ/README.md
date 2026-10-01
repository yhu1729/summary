# 2026JHJ

## ChatGPT (September 2026)

### Summary

This paper develops a discontinuous Galerkin solver for nonrelativistic particle kinetics on smooth, time-independent manifolds. Hamiltonian formulations encode curved geometry in either canonical or noncanonical coordinates. With a continuous discrete Hamiltonian, the collisionless scheme conserves particle number and energy; the noncanonical form also requires a continuous Poisson tensor. In canonical coordinates, central fluxes conserve the phase-space $L^2$ norm, while upwind fluxes make it decay. An implicit Bhatnagar–Gross–Krook (BGK) collision step, which relaxes the distribution toward local equilibrium, uses iterative moment corrections to preserve density, momentum, and energy. Shock and Kelvin–Helmholtz tests on flat, spherical, and hyperbolic geometries, including a rotating sphere, demonstrate the method. In the strongly collisional limit, the shock solution approaches the curved-manifold Euler result. The noncanonical momentum representation can reduce geometry-induced resolution demands, although the paper does not establish the same $L^2$ stability for it. A general relativistic extension remains future work.

### Contributions

1. Derived canonical and noncanonical Hamiltonian kinetic equations for particle motion on smooth manifolds.
2. Constructed a discontinuous Galerkin discretization with discrete particle-number and energy conservation under stated continuity conditions.
3. Proved $L^2$ conservation for central fluxes and monotone $L^2$ decay for upwind fluxes in the canonical collisionless scheme.
4. Coupled an implicit BGK operator to iterative corrections that preserve its density, momentum, and energy moments.
5. Demonstrated curved-surface shocks, Kelvin–Helmholtz instability, rotation, and recovery of the Euler limit at high collisionality.
