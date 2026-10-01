# 2026GILO

## ChatGPT (July 2026)

### Summary

Summation-by-parts identities provide discrete conservation and energy estimates, but this paper shows that satisfying the formal SBP definition does not ensure an accurate differentiation operator. Counterexamples for linear advection exhibit conservative, energy-stable function-space SBP operators with severe errors and poor convergence because unresolved modes remain in the differentiation matrix's nullspace. The authors make nullspace consistency and approximation outside the exactness space explicit design requirements. They then extend an optimization-based construction of function-space SBP operators in two ways. A prescribed sparse block or band structure reduces the differentiation-matrix optimization from $O(N^2)$ to $O(Nb)$ unknowns and can restore useful nullspace and error behavior for global operators. For local operators, regularization minimizes derivative errors on an augmented function set when exactness on the larger space is impossible. Linear-advection and manufactured two-dimensional Euler tests show sparse operators outperforming dense counterparts and regularized operators outperforming unregularized ones. The framework applies to arbitrary one-dimensional nodes and finite-dimensional function spaces, with higher-dimensional use through tensor products.

### Contributions

1. Demonstrated that algebraic SBP exactness, positive norm, conservation, and energy stability can coexist with poor approximation and convergence.
2. Identified unresolved nullspace modes and failure of nullspace consistency as the central structural cause of inaccurate solutions.
3. Formulated augmented-basis derivative-error minimization as an additional accuracy criterion beyond formal SBP exactness.
4. Introduced a sparse parameterization that reduces optimization unknowns from $O(N^2)$ to $O(Nb)$ and makes global function-space SBP operators more practical.
5. Validated sparse and regularized constructions on one-dimensional advection and manufactured two-dimensional compressible Euler problems.
