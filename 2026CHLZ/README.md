# 2026CHLZ

## ChatGPT (July 2026)

### Summary

The paper proposes augmented block conjugate gradients for a single symmetric positive-definite system: append a Gaussian random block to the right-hand side and solve in their joint block Krylov space. Although no preconditioner is formed, a deterministic subspace-containment theorem shows that the method implicitly contains the iterates of preconditioned conjugate gradients for a broad family of Nyström deflation preconditioners. Consequently, after equal numbers of matrix loads, augmented block conjugate gradients is never worse than the corresponding Nyström-preconditioned method in exact arithmetic. Probabilistic bounds relate convergence to the condition number remaining after dominant eigenvalues are removed, and new guarantees for deeper Krylov Nyström preconditioners follow along the way. Shift invariance lets one block-Lanczos factorization solve many $(A+\mu I)x=b$ systems, making the approach attractive for an entire ridge-regression regularization path. Integrating these shifted solves also gives guarantees for generating multiple Gaussian samples via matrix square roots. Experiments show substantial improvements when loading the matrix dominates cost, while the authors explicitly note extra arithmetic, storage, and finite-precision issues for block Lanczos.

### Contributions

1. Introduced randomized augmented block conjugate gradients using Gaussian auxiliary right-hand sides as implicit spectral information.
2. Proved Krylov-subspace containment and deterministic same-matrix-load dominance over a broad class of Nyström-preconditioned methods.
3. Derived probabilistic convergence and matrix-vector complexity bounds through deeper-Krylov Nyström-preconditioning estimates.
4. Exploited shift invariance to evaluate many regularization parameters from one block-Lanczos run for ridge-regression paths.
5. Extended the analysis to matrix-square-root iterations for multiple Gaussian samples and verified the gains experimentally.
