# 2026BBKL

## ChatGPT (July 2026)

### Summary

This preprint applies reduced rank extrapolation (RRE) to splitting-based fixed-point solvers for generalized multi-term Sylvester equations, including Lyapunov-plus-positive problems. For small dense equations, cycling RRE forms extrapolants from windows of matrix iterates and can improve the asymptotic reduction factor by suppressing dominant iteration modes. For large sparse equations, the authors extend RRE to nonsymmetric low-rank factors and embed it in a nonstationary outer iteration whose inner Sylvester solves use dynamically adjusted tolerances. Rank truncation controls storage, and factored residual estimators avoid assembling dense residual matrices. Convergence results cover exact stationary and inexact nonstationary processes. Dense and low-rank experiments using ADI or extended Krylov inner solvers show that suitable RRE windows reduce outer iterations, runtime, and often memory, although performance depends on window size and extrapolation can increase intermediate ranks.

### Contributions

1. Extended cycling RRE to fixed-point iterations for multi-term Sylvester equations.
2. Derived convergence results for exact stationary and inexact nonstationary iterations.
3. Generalized RRE to sequences of nonsymmetric low-rank matrix approximations.
4. Integrated adaptive inner tolerances, rank truncation, and cheap residual estimation.
5. Demonstrated iteration, runtime, and storage reductions in dense and large-scale tests.
