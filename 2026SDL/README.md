# 2026SDL

## ChatGPT (July 2026)

### Summary

The authors develop higher-order residual-based variational multiscale (VMS) schemes for incompressible turbulent flow using half-explicit Runge--Kutta (HERK) integration. Applying time discretization before space discretization respects the Navier--Stokes equations' index-2 differential--algebraic structure and avoids the order reduction of conventional multistage treatments. Each Runge--Kutta stage produces a Darcy-like subproblem, allowing the subgrid stabilization parameter to be derived analytically by bubble enrichment without additional linearization assumptions. Fourier dispersion--dissipation analysis shows favorable spectral behavior. Algebraic scaling isolates all stage and time-step dependence, so a single symmetric block matrix can be reused across stages and steps, reducing memory and solve cost. Taylor--Green vortex tests improve energy-spectrum and dissipation predictions over generalized-$\alpha$ VMS, while open-cavity simulations recover the theoretical Hopf threshold and limit-cycle amplitude. Explicit convection and viscosity impose a stricter stability limit, but the method supplies accurate high-order dynamics for transient and turbulent flows.

### Contributions

1. Formulated HERK-based VMS discretizations consistent with the index-2 incompressible-flow system.
2. Derived a subgrid stabilization parameter from bubble enrichment of the stagewise Darcy problem.
3. Established improved dispersion--dissipation behavior for the resulting space--time discretization order.
4. Reused one symmetric block matrix across Runge--Kutta stages and time steps.
5. Improved turbulent-spectrum, dissipation, Hopf-threshold, and limit-cycle predictions in benchmark flows.
