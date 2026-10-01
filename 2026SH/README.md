# 2026SH

## ChatGPT (July 2026)

### Summary

The study evaluates a single-source fluid solver that combines nodal discontinuous Galerkin spatial discretization, explicit Runge--Kutta time integration, MPI domain decomposition, and Kokkos portability across CPUs and GPUs. The code solves linear advection and isothermal Euler equations in one, two, and three dimensions with spatial orders through eight and temporal orders through six. Fixed-accuracy experiments show that high-order discretizations require far fewer degrees of freedom and less runtime than third- or fourth-order alternatives despite greater per-step cost; classical fourth-order Runge--Kutta generally offers a practical temporal balance. Local element operations map effectively to many-core hardware, and the same implementation exhibits near-perfect weak scaling beyond 6,000 CPU cores and across 64 GPUs without architecture-specific rewrites. Hardware comparisons reveal a workload-size crossover: CPUs are faster and can use less energy for small grids, while GPUs dominate large cases above roughly $10^7$ degrees of freedom. Energy estimates also expose a rebound effect, because newer GPUs require increasingly large problems to realize their efficiency advantage. The benchmarks support portable high-order simulation, but cover a limited equation set and defer direct comparison with pseudo-spectral solvers and architecture-specific tuning.

### Contributions

1. Implemented a portable high-order fluid solver combining nodal discontinuous Galerkin, Runge--Kutta, MPI, and Kokkos.
2. Quantified the memory and runtime advantage of eighth-order spatial accuracy at fixed global error.
3. Demonstrated one code base across multiple CPU and GPU vendors without substantial architecture-specific tuning.
4. Measured near-perfect weak scaling beyond 6,000 CPU cores and on 64 GPUs.
5. Established problem-size-dependent CPU/GPU performance and energy crossovers, including a hardware-generation rebound effect.
