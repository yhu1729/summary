# 2025P

## ChatGPT (July 2026)

### Summary

The paper develops multi-order Runge--Kutta methods that act directly on initial-value problems of arbitrary differential order instead of first rewriting them as first-order systems. Starting from Taylor's theorem with integral remainder and Gauss--Jacobi quadrature, it constructs stage formulas that approximate the solution and its derivatives together. A directed maximum-weight graph records stage dependencies; strongly connected components identify implicit blocks, while independent blocks expose possible parallelism. This graph-based view yields an intrinsic definition of explicitness invariant under stage permutations. The paper defines consistency separately by derivative rank, derives order conditions and convergence results, and studies how reducing, prolonging, or overwriting an initial-value problem affects accuracy. Numerical experiments on a sixth-order linear problem show much smaller local errors than matched classical Runge--Kutta schemes, although unstable large steps can erase that advantage. The stability theory generalizes A- and L-stability, proves a multi-order analogue of the second Dahlquist barrier, and introduces half-line stability. Appendices provide Rust-oriented implementation details and extensive solved order conditions.

### Contributions

1. Defined a Runge--Kutta framework that directly advances arbitrary-order initial-value problems and their derivatives.
2. Derived the methods from Taylor integral formulas and Gauss--Jacobi quadrature without differentiating the right-hand side.
3. Introduced weight digraphs, implicit blocks, implicit rank, and parallel blocks to characterize stage-system structure.
4. Established rank-dependent consistency, convergence, rewriting, and order-condition theory.
5. Generalized A- and L-stability, introduced half-line stability, and supplied numerical comparisons and an implementation framework.
