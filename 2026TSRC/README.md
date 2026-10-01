# 2026TSRC

## ChatGPT (July 2026)

### Summary

The authors construct a fully analytical manufactured solution for the collisionless electrostatic gyrokinetic Vlasov--Poisson model with adiabatic electrons in cylindrical geometry. Its spatially varying magnetic field, density, electrostatic potential, gyroaveraging, and $\nabla B$ drift exercise central gyrokinetic particle-in-cell operations while parameters suppress boundary contamination. Extending earlier Vlasov--Poisson analysis, they prove that convergence of the electric field--and, through elliptic regularity, the mesh charge density--is sufficient to establish convergence of the particle-represented distribution, avoiding direct noisy phase-space reconstruction. They implement the forced problem in XGC and perform simultaneous refinements of mesh spacing, timestep, and particles per vertex. XGC exhibits the expected second-order temporal and Monte Carlo $N_p^{-1/2}$ behavior. Spatial convergence lies between first and second order: lumping the finite-element mass matrix makes the particle-to-mesh density gather formally first order locally, while mesh symmetry improves the global $L^2$ behavior to about $O(\Delta r^{3/2})$.

### Contributions

1. Derived a manufactured solution exercising gyroaveraging, $\nabla B$ drift, and the gyrokinetic Poisson solve.
2. Extended deterministic PIC verification theory to forced multidimensional gyrokinetic systems.
3. Proved that field or mesh-density convergence verifies the represented distribution.
4. Integrated the forcing into XGC and verified timestep and particle-number scaling.
5. Diagnosed fractional global spatial convergence from lumped-mass gathering and mesh geometry.
