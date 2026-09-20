# 2025DFHL

## ChatGPT (July 2026)

### Summary

Solving $AX+XB=C$ with a low-precision Schur decomposition can save work, but the resulting quasi-triangular factors are perturbed and their Schur vectors are not unitary to working precision. This paper derives an iterative-refinement scheme for perturbed quasi-triangular Sylvester equations, with sufficient convergence conditions and a bound on the attainable relative residual. It then builds two mixed-precision solvers: both compute Schur data and an approximate solution in low precision, refine the triangular solve in working precision, and recover the original solution either by re-orthonormalizing the Schur vectors or explicitly inverting the nearly unitary factors. The authors also analyze Schur-preconditioned GMRES refinement and find it generally less accurate and more expensive in the two-precision setting. Tests on Sylvester and Lyapunov problems match the accuracy of high-precision Bartels--Stewart methods. Operation-count models predict speedups on hardware with sufficiently fast native low precision, rather than reporting measured wall-clock gains.

### Contributions

1. Developed iterative refinement for perturbed quasi-triangular Sylvester equations.
2. Proved sufficient convergence conditions and bounded the attainable relative residual.
3. Constructed two mixed-precision solvers using re-orthonormalization or explicit inversion of Schur factors.
4. Explained why Schur-preconditioned GMRES refinement is unattractive in the targeted two-precision regime.
5. Demonstrated high-precision accuracy and quantified conditions under which low-precision work should reduce cost.
