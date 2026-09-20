# 2025DS

## ChatGPT (July 2026)

### Summary

Jacobi diagonalization, Gaussian elimination, and Gram--Schmidt appear to solve different matrix factorizations, yet each repeatedly transforms selected columns. The paper places one- and two-sided variants of these algorithms in a common procedure that can produce eigendecompositions, singular value decompositions, Cholesky factorizations, or QR factorizations by constraining each local transformation. It then chooses a subset of $k$ indices uniformly at random and exactly factors the corresponding principal block. A potential function measuring normalized nonorthogonality or nondiagonality yields the same expected linear contraction factor, $1-k(k-1)/(n(n-1))$, for every supported factorization. Consequently, sufficiently well-conditioned inputs reach an approximate factorization in $O(n^2\log(n\widehat{\kappa}/\delta))$ pairwise-size iterations, and the analysis also confirms a conjectured convergence rate for the Kaczmarz--Kac orthogonalization walk. For finite arithmetic, martingale arguments control accumulated local errors and show stability for a broad class of randomized orthogonalization methods. Applied to randomized Jacobi iteration, the analysis bounds the diagonal-normalized condition numbers of all iterates polynomially with high probability. This supplies the missing theoretical condition behind Demmel and Veselić's relative-accuracy analysis without preconditioning. The precision exponents are explicit but not optimized, so the results establish polynomial stability rather than practical superiority at standard precision.

### Contributions

1. Unified Jacobi eigendecomposition and SVD algorithms with elimination and Gram--Schmidt methods for Cholesky and QR factorizations.
2. Defined a uniformly random size-$k$ pivoting rule applicable across the entire factorization class.
3. Proved a factorization-independent expected linear convergence rate using a common potential function.
4. Derived finite-precision stability guarantees for a broad family of randomized orthogonalization procedures through martingale error control.
5. Proved polynomial high-probability control of Jacobi iterates' normalized condition numbers, resolving the unproved assumption in the Demmel--Veselić analysis.
