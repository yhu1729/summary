# 2026QNC

## ChatGPT (July 2026)

### Summary

This paper extends entropy-stable reduced-order modeling for nonlinear conservation laws from finite-volume to high-order discontinuous Galerkin full-order models. A mass-matrix-aware weighted test basis supports two-stage hyper-reduction; under ideal hyper-reduction, the resulting differentiation-matrix error is orthogonal to the ROM approximation space. Dimension-by-dimension sampling reduces multidimensional volume flux evaluations, while numerical-linear-algebra-based Carath\'eodory pruning hyper-reduces boundary terms without a sparsity-promoting linear-programming solver and gives a predictable number of boundary nodes. Artificial-viscosity terms are projected to dissipate entropy. One- and two-dimensional advection, Burgers, and Euler tests with periodic and weakly imposed reflective boundaries keep convective entropy near machine precision and show viscous entropy dissipation, with useful speedups for small bases. The method does not provide a rigorous error analysis, relies on simple artificial viscosity and linear proper-orthogonal-decomposition spaces, and therefore does not resolve the known accuracy difficulty of transport-dominated solutions.

### Contributions

1. Generalized entropy-stable reduced-order model construction from finite-volume to high-order discontinuous Galerkin full-order models.
2. Introduced a mass-matrix-aware weighted test basis and established ideal hyper-reduction error orthogonality.
3. Developed dimension-by-dimension volume hyper-reduction for multidimensional discontinuous Galerkin flux differencing.
4. Replaced linear-programming-based boundary sparsification with Carath\'eodory pruning having predictable sample counts.
5. Validated entropy behavior, accuracy, and runtime on one- and two-dimensional nonlinear conservation laws with periodic and reflective boundaries.
