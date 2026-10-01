# 2026AVZ

## ChatGPT (September 2026)

### Summary

This paper computes singly diagonally implicit Runge--Kutta (SDIRK) stages through an explicit stabilized iteration. It rewrites the implicit stage equations as the steady state of an auxiliary system, then applies a partitioned Runge--Kutta--Chebyshev iteration. The partition isolates diagonal diffusion from off-diagonal diffusion and advection, avoiding large Newton systems; stiff reactions require only local Jacobian inversions. For linear diffusion, the authors prove convergence independently of spatial dimension and a cost of $O(\sqrt{\Delta t}/\Delta x)$ diffusion evaluations per SDIRK step on a grid of spacing $\Delta x$. For linear advection--diffusion, they prove convergence under stated spectral and stability conditions. An adaptive fourth-order implementation, exSDIRK4, is tested on one- and two-dimensional Brusselator problems. Compared with second-order PIROCK, it uses more evaluations at loose tolerances but becomes more efficient as accuracy demands increase. The analysis does not extend directly to fully implicit Runge--Kutta methods.

### Contributions

1. Recast SDIRK stage equations as a steady-state problem solvable by explicit stabilized iteration.
2. Split the stage operator so diffusion drives Chebyshev stabilization, while stiff reactions use spatially local Jacobian inversions.
3. Proved dimension-independent convergence for linear diffusion and the stated $O(\sqrt{\Delta t}/\Delta x)$ diffusion-evaluation cost.
4. Established conditional convergence for linear advection--diffusion and analyzed the iteration's diffusion--advection stability region.
5. Built an adaptive fourth-order implementation and demonstrated its cost advantage over PIROCK at tight tolerances on stiff Brusselator tests.
