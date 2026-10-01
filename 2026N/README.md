# 2026N

## ChatGPT (July 2026)

### Summary

This paper studies differential inversion of the implicit Euler map $E(t,m,x)$: computing $(E')^{-1}v$ without explicitly accumulating and inverting its full Jacobian. Three approaches are compared. Naive algorithmic differentiation through Newton solves costs $\mathcal{O}(mpn^4)$; a partially symbolic implicit-function treatment reduces this to $\mathcal{O}(mn^3)$. The new fully symbolic method stores elemental Jacobians during the $m$ Euler steps and propagates inverse actions backward through matrix-vector products, yielding $\mathcal{O}(mn^2)$ work and $\mathcal{O}(mn^2)$ storage. A C++ reference implementation using Eigen and dco/c++ tests Lotka-Volterra systems. Runtime scaling supports the theoretical advantage, while memory measurements show that the stored tape dominates the fully symbolic method. Checkpointing can trade recomputation for memory. The analysis assumes differential invertibility and sufficiently converged nonlinear solves; regularization for ill-posed inverse problems remains future work.

### Contributions

1. Formulated inverse-Jacobian actions for implicit Euler integration as a differential-inversion problem.
2. Separated naive, partially symbolic, and fully symbolic algorithms with explicit complexity estimates.
3. Derived reverse elemental propagation that avoids both global Jacobian accumulation and a final dense solve.
4. Reduced asymptotic work to $\mathcal{O}(mn^2)$, an $\mathcal{O}(n^2)$ improvement over the naive route.
5. Supplied reproducible C++ implementations and runtime, memory, and numerical-accuracy experiments.
