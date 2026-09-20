# 2026FPKA

## ChatGPT (July 2026)

### Summary

The paper develops particle-in-cell discretizations and discrete-gradient time integrators for both the Hamiltonian Vlasov-Poisson subsystem and dissipative Landau collisions, viewing their combination as a metriplectic system. Spatial bracket discretizations preserve the relevant degeneracies, while the time-discrete constructions conserve mass, momentum, and energy and maintain entropy-production monotonicity up to nonlinear-solver tolerances. PETSc implementations are tested on collisionless Landau damping and electron-positron thermal equilibration. In damping tests, discrete gradients match symplectic accuracy and outperform RK4 in preserving invariants, but implicit solves cost roughly 130% more per step than symplectic integration and 160% more than RK4. In equilibration, the integrator preserves momentum to $O(10^{-13})$, kinetic energy to $O(10^{-12})$, and monotone entropy until equilibrium-scale solver fluctuations. The work supplies an open-source, cross-verified structure-preserving Landau implementation while identifying nonlinear-solver efficiency as the main limitation.

### Contributions

1. Placed Vlasov-Poisson and Landau particle discretizations in one metriplectic structure-preserving framework.
2. Derived a discrete-gradient Landau integrator that conserves moments and enforces entropy monotonicity.
3. Avoided Gonzalez-gradient singularities near equilibrium through an alternative discrete-gradient choice.
4. Implemented Hamiltonian and collisional integrators in PETSc with nonlinear-solver tolerance studies.
5. Quantified conservation, entropy, and runtime trade-offs on Landau damping and two-species equilibration.
