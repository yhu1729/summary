# 2025DDGG

## ChatGPT (July 2026)

### Summary

Weakly collisional magnetic-mirror transport spans fast ion transit and slow collision times, while strong mirror forces impose prohibitive explicit time steps. This work adapts COGENT's implicit-explicit continuum kinetic framework to 1D--2V simulations with kinetic ions, nonlinear Fokker--Planck collisions, beam fueling, and Boltzmann electrons under WHAM-relevant parameters. High-order additive Runge--Kutta integration treats the Vlasov operator implicitly through Jacobian-free Newton--Krylov iterations, with an approximate-ideal-restriction algebraic multigrid preconditioner built from a lower-order discretization. Stable steps reach $2.5\times10^4$ times the explicit CFL limit and yield about a 2500-fold speedup, allowing a 20 ms low-resolution run in roughly 25 minutes on 512 cores. A fully implicit 0D--2V bounce-averaged square-mirror model reproduces the analytic Pastukhov confinement problem and helps assess phase-space resolution. It reveals first-order convergence when the loss-cone transition is under-resolved and substantial differences between nonlinear Fokker--Planck and simplified Lenard--Bernstein--Dougherty collisions. Fifth-order upwinding is necessary to control long-time numerical diffusion. The present Boltzmann-electron model, fixed-field preconditioner, and baseline resolution limit accuracy outside the trap and omit kinetic-electron and unlike-species effects.

### Contributions

1. Developed a semi-implicit COGENT formulation for full-$F$ continuum kinetic transport in strongly magnetized mirror geometry.
2. Combined Jacobian-free Newton--Krylov iteration with approximate-ideal-restriction multigrid preconditioning for the stiff Vlasov solve.
3. Achieved time steps $2.5\times10^4$ above the explicit limit and approximately 2500-fold end-of-run speedup.
4. Implemented and verified a bounce-averaged square-mirror model against the analytic Pastukhov problem.
5. Exposed resolution-sensitive loss-cone convergence, collision-operator differences, and the need for fifth-order upwinding over collisional timescales.
