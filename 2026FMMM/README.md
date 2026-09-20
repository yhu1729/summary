# 2026FMMM

## ChatGPT (July 2026)

### Summary

The paper develops a method-of-manufactured-solutions framework for three-dimensional particle-in-cell simulations with direct-simulation Monte Carlo binary elastic collisions. Rather than evolving manufactured particle weights, it manufactures separable phase-space distributions and uses inverse cumulative distributions to define exact particle positions and velocities, avoiding negative weights and interference with weight-dependent collision logic. Collision effects are verified by averaging independent stochastic outcomes and deriving an analytic velocity source from manufactured cross sections and angular anisotropy. Error models couple spatial and temporal discretization, finite-particle sampling, and collision statistics. Across uncoupled, one-way-coupled, and fully coupled tests, particle and potential errors recover second-order convergence with one run per discretization; isolated collision error behaves as $O(h^2)$ in the maximum norm and approximately $O(h^{5/2})$ in the $L^2$ norm. Complementary scattering-angle tests expose an injected collision error that trajectory metrics miss, while another injected error shows the reverse. Charged-particle Coulomb collision extensions are outside scope.

### Contributions

1. Constructed exact manufactured particle trajectories by inverse sampling without changing weights.
2. Derived an analytic manufactured collision source from averaged stochastic outcomes.
3. Derived refinement rates for coupled discretization, sampling, and collision errors.
4. Recovered expected second-order convergence across multiple three-dimensional coupling cases.
5. Showed that trajectory and scattering-angle metrics detect complementary collision bugs.
