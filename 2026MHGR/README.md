# 2026MHGR

## ChatGPT (July 2026)

### Summary

This survey updates the description of Trilinos for heterogeneous, leadership-scale computing. It organizes more than 35 packages into five product areas: Core, Linear Solvers and Preconditioners, Nonlinear Solvers and Analysis Tools, Discretization Tools, and Framework. The modern stack replaces archived Epetra-era components with Kokkos-enabled successors centered on Tpetra, using execution and memory-space abstractions to support CPUs and accelerators from one source base. The paper maps distributed linear algebra, load balancing, Krylov and direct solvers, domain decomposition, multigrid, eigensolvers, nonlinear solution, optimization, automatic differentiation, uncertainty quantification, time integration, finite elements, and meshfree approximation onto this structure. It also documents the TriBITS-based build and test system, documentation infrastructure, PyTrilinos2 bindings, package-quality expectations, contribution pathways, and links to external scientific-software communities. The result is a current architectural and organizational reference rather than a performance benchmark.

### Contributions

1. Reorganized the modern Trilinos ecosystem into five coherent product areas and mapped its packages to them.
2. Explained how Kokkos and Tpetra provide performance-portable execution, memory management, and distributed linear algebra.
3. Catalogued the current solver, analysis, and discretization capabilities and their package-level interfaces.
4. Documented build, continuous-testing, documentation, and Python-binding infrastructure for users and developers.
5. Described governance, contribution expectations, onboarding channels, and integration with the wider high-performance software ecosystem.
