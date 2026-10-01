# 2025PLGC

## ChatGPT (July 2026)

### Summary

This paper describes a multigrid Poisson solver for adaptive multiresolution grids, targeting unbounded and semi-unbounded domains common in computational physics. The solver is implemented in the murphy framework for partial differential equations on collocated adaptive grids. Its main design combines multigrid iteration with a Fourier-based direct solve, giving flexibility for boundary-condition combinations that include periodic, unbounded, and semi-unbounded directions. High-order compact stencils are used to improve accuracy while reducing communication compared with wider discretizations. The method is validated against analytical solutions in periodic and unbounded settings. The implementation is also tested at large scale, with reported scalability to 16,384 cores on major European high-performance computing systems. The paper therefore contributes both a numerical method and an implementation strategy for the Poisson equation, often the dominant cost in incompressible-flow and related adaptive-grid simulations.

### Contributions

1. Implemented a flexible multigrid Poisson solver in an adaptive multiresolution framework.
2. Combined multigrid iteration with Fourier direct solvers for unbounded boundary conditions.
3. Used high-order compact stencils to improve accuracy and reduce communication.
4. Validated the solver against analytical periodic and unbounded-domain solutions.
5. Demonstrated large-scale parallel scalability to 16,384 cores.
