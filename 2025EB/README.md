# 2025EB

## ChatGPT (July 2026)

### Summary

Per-iteration bounds for randomized Gauss--Seidel and Kaczmarz methods are often much slower than observed convergence and incorrectly suggest that relaxation can only hurt. This paper instead studies the global asymptotic rate, which is governed almost surely by a Lyapunov exponent of random projector products. The authors bound that exponent through the spectral radius of the covariance-evolution superoperator $\mathcal{A}=\mathbb{E}[(I-\omega P)\otimes(I-\omega P)]$. A new min--max argument, connected to Perron--Frobenius theory for positive maps on noncommutative algebras, produces an asymptotic A-bound using the two smallest eigenvalues of $\mathbb{E}[P]$ and a fourth-order statistic. The bound is strictly sharper than the standard per-iteration B-bound when the spectral gap is positive. Its closed-form minimizing relaxation parameter is provably faster than $\omega=1$, explaining over-relaxation and resolving the cited open question. Experiments show much tighter predictions across tested matrices.

### Contributions

1. Reframed randomized Gauss--Seidel and Kaczmarz convergence through global asymptotic Lyapunov rates.
2. Connected the rate to a covariance superoperator governed by noncommutative Perron--Frobenius theory.
3. Developed a new spectral-radius bound using second- and fourth-order projector statistics.
4. Proved when the asymptotic A-bound improves on the standard per-iteration B-bound.
5. Derived a provably beneficial relaxation parameter and validated the tighter rate predictions numerically.
