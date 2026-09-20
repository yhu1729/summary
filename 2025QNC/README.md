# 2025QNC

## Codex/ChatGPT (July 2026)

### Summary

This paper extends entropy-stable reduced order modeling for nonlinear conservation laws from finite volume full-order models to high-order discontinuous Galerkin full-order models. The authors adapt flux-differencing and entropy-projection ideas to DG mass matrices and introduce a weighted test basis that improves hyper-reduced differentiation accuracy. They prove that, under ideal hyper-reduction, the differentiation-matrix approximation error is orthogonal to the ROM space when measured with the modified test basis. For boundary terms, they replace linear-programming-based sparsification with a numerical-linear-algebra Caratheodory pruning procedure that gives a predictable number of boundary sample nodes. Tests on one- and two-dimensional problems with periodic and weakly imposed boundary conditions show convective entropy contributions near machine precision and viscous entropy dissipation. The resulting ROMs remain stable with small numbers of modes and hyper-reduced volume and boundary nodes, while the paper identifies rigorous error analysis and transport-dominated accuracy as important open problems.

### Contributions

1. Generalized entropy-stable ROM construction from finite volume to high-order DG full-order models.
2. Introduced a weighted test basis for DG-compatible two-step hyper-reduction.
3. Proved an orthogonality property for ideal hyper-reduced differentiation errors.
4. Developed Caratheodory pruning for entropy-stable boundary hyper-reduction without LP solvers.
5. Validated entropy stability on nonlinear conservation-law tests with periodic and weak boundary conditions.
