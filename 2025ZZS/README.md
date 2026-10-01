# 2025ZZS

## ChatGPT (July 2026)

### Summary

This work extends diagonalization-based parallel-in-time integration to nonlinear evolution equations containing first-, second-, or third-order time derivatives. A hybrid finite-difference formula produces an all-at-once time matrix $B$. For nonlinear problems, a simplified quasi-Newton iteration replaces the time-dependent block Jacobians by their average, preserving a Kronecker structure. Diagonalizing $B=VDV^{-1}$ then decouples each iteration into independent shifted spatial systems that can be solved concurrently across time modes; higher-order equations are reduced to equivalent systems involving powers of $B$. By relating the characteristic equation to Chebyshev polynomials, the authors derive explicit eigenvalues and eigenvectors, prove $\operatorname{cond}_2(V)=\mathcal{O}(n^3)$, and construct an $\mathcal{O}(n^2)$ algorithm for $V^{-1}$. At $n=8192$, the reported spectral-decomposition implementation is about ten times faster than MATLAB's `eig`-based route, although the reconstruction residual worsens with $n$ because $V$ is increasingly ill-conditioned. Four two-dimensional second- and third-order examples show decreasing runtime through 20 CPU cores, with diminishing returns from communication. The experiments establish feasibility and parallel speedup, but do not compare solution time or robustness against other modern parallel-in-time methods.

### Contributions

1. Extended a direct diagonalization-based parallel-in-time formulation to nonlinear equations with time derivatives through third order.
2. Preserved separability for nonlinear problems through an average-Jacobian simplified quasi-Newton iteration.
3. Derived explicit spectral factors of the all-at-once time matrix using Chebyshev-polynomial identities.
4. Proved cubic growth of the eigenvector condition number and developed an $\mathcal{O}(n^2)$ inverse-eigenvector algorithm.
5. Demonstrated spectral-decomposition and multicore speedups on second- and third-order partial-differential-equation examples.
