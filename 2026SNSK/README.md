# 2026SNSK

## ChatGPT (July 2026)

### Summary

This paper constructs an $L^2$-conforming discontinuous Galerkin discretization of Liu's consistent splitting scheme for incompressible Navier--Stokes flow. Each time step decouples pressure and velocity into one pressure Poisson solve followed by one vector convection--diffusion--reaction solve. Consistent pressure boundary conditions cover Dirichlet, open, and traction boundaries, avoiding the artificial pressure boundary layers and temporal splitting errors of standard projection methods. Symmetric interior penalty handles second derivatives, while linearly implicit convection relaxes explicit CFL restrictions without requiring nonlinear solves. A Leray projection together with divergence and normal-continuity penalties improves mass conservation. Manufactured-solution tests recover optimal spatial and temporal rates, including higher-order BDF formulas, and cylinder-flow and three-dimensional Taylor--Green-vortex benchmarks agree with established solvers. The analysis also identifies a lowest-order accuracy limitation when the viscous curl--curl term is under-resolved.

### Contributions

1. Formulated an $L^2$ discontinuous Galerkin consistent-splitting method for incompressible flow.
2. Derived consistent pressure boundary treatments for closed, open, and traction boundaries.
3. Combined linearly implicit convection with decoupled pressure and momentum solves.
4. Improved discrete mass conservation using Leray, divergence, and normal-continuity stabilization.
5. Verified high-order convergence and benchmark accuracy for two- and three-dimensional flows.
