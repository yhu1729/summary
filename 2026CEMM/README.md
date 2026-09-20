# 2026CEMM

## ChatGPT (July 2026)

### Summary

Randomized block Krylov iteration computes a rank-$k$ matrix approximation by repeatedly multiplying a target matrix by a random starting block of $b$ vectors. Previous near-optimal theory covered only $b=1$ and $b=k$; bounds for intermediate blocks contained a $b(k-b)$ factor and could require $O(k^2)$ matrix--vector products, despite intermediate block sizes often performing best in practice. This paper closes that gap. For every $1\leq b\leq k$, it proves that randomized block Krylov iteration obtains a $(1+\varepsilon)$-factor approximation to the best rank-$k$ approximation using $\widetilde O(k/\sqrt{\varepsilon})$ matrix--vector products, with both Frobenius- and spectral-norm guarantees and associated singular-vector capture. The proof reduces the approximation analysis to conditioning of a square random block Krylov matrix. New lower bounds on its minimum singular value combine Gaussian anti-concentration, Vandermonde structure, and a non-sparsification argument; the conditioning results may also inform sparse linear-system algorithms. The theorem supplies theoretical support for practical intermediate block sizes without claiming that all choices have equal wall-clock cost. Remaining questions include sharper singular-gap dependence, removing condition-number terms, finite-precision behavior, and sparse random starting blocks.

### Contributions

1. Proved near-optimal randomized block Krylov guarantees for every block size $1\leq b\leq k$.
2. Removed the prior worst-case $b(k-b)$ dependence from matrix--vector-product complexity.
3. Established $(1+\varepsilon)$ low-rank approximation guarantees in Frobenius and spectral norms.
4. Reduced the analysis to quantitative conditioning of square random block Krylov matrices.
5. Developed minimum-singular-value bounds using anti-concentration, Vandermonde structure, and non-sparsification.
