# 2026A

## ChatGPT (July 2026)

### Summary

Semi-Lagrangian discontinuous Galerkin (SLDG) methods can take large time steps for kinetic transport, but their usual precomputed overlap matrices assume uniform cell widths. This paper extends SLDG to adaptively refined velocity meshes and from one to three velocity dimensions for the Vlasov--Poisson system. A hybrid sweep uses precomputed level-specific overlap matrices on conforming cells and evaluates generalized overlap integrals only at nonconforming refinement interfaces. A compressed-sparse-row pencil representation organizes dimensionally split sweeps, including weighted accumulation when coarse cells occur in multiple pencils. Tensor-product discontinuous Galerkin elements on PETSc hexahedral meshes provide the three-dimensional velocity discretization. A $1X+3V$ Landau-damping test reproduces the expected damping behavior, conserves mass exactly, and shows convergence with polynomial degree and adaptive-refinement level. The work establishes the algorithmic machinery and baseline verification for adaptive high-dimensional SLDG; broader nonlinear plasma tests and performance/scalability characterization are not presented in the reported study.

### Contributions

1. Extended semi-Lagrangian discontinuous Galerkin transport to adaptively refined, nonuniform velocity meshes.
2. Introduced fast conforming-cell sweeps and on-demand generalized overlap integration at refinement boundaries.
3. Designed a compressed-sparse-row pencil structure for dimensionally split adaptive sweeps.
4. Generalized the method to three velocity dimensions using tensor-product PETSc finite elements.
5. Verified damping rates, exact mass conservation, and convergence on a $1X+3V$ Landau-damping problem.
