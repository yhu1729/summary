# 2026KW

## ChatGPT (July 2026)

### Summary

This paper unifies partial pivoted Cholesky and Vecchia approximations for large positive-semidefinite matrices. Its central theorem shows that adding a Vecchia approximation of a partial-Cholesky residual gives exactly a Vecchia approximation of the original matrix with an augmented inverse-Cholesky sparsity pattern. The hybrid construction needs $O(rn)$ target-entry accesses rather than $O(r^2n)$ in the stated regime. The authors extend Vecchia optimality in the Kaporin condition number to positive-semidefinite targets and derive bounds connecting that quantity to linear solves and determinant estimation. They compare adaptive search, randomized and greedy pivots, nearest neighbors, and orthogonal matching pursuit. Experiments use 22 machine-learning datasets, each with 20,000 observations, and Gaussian kernel matrices at three regularization levels. Partial Cholesky plus Vecchia generally outperforms earlier Cholesky-derived preconditioners, but none of the tested methods solves half of the most nearly singular cases.

### Contributions

1. Proved that partial Cholesky plus a Vecchia residual approximation equals one augmented-pattern Vecchia approximation.
2. Reduced target-matrix entry accesses from $O(r^2n)$ to $O(rn)$ in the analyzed regime.
3. Extended Kaporin-condition-number optimality from positive-definite to positive-semidefinite target matrices.
4. Derived Kaporin-based guarantees for linear solves and determinant estimates.
5. Compared pivot and sparsity strategies on 22 large kernel datasets and documented their near-singular limitations.
