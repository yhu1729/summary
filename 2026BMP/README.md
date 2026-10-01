# 2026BMP

## ChatGPT (July 2026)

### Summary

This paper compares momentum-accelerated power iteration with restarted Lanczos for dominant eigenpairs of symmetric or Hermitian matrices using matrix-vector products as the common cost. Both methods apply polynomial filters whose convergence is governed by Chebyshev-polynomial ratios, but their suppression of subdominant eigenmodes differs: momentum has a nearly uniform average rate with oscillations, whereas restarted Lanczos has quasi-periodic mode-wise behavior. The analysis derives a critical Krylov subspace size $m_c$, determined by relative spectral-gap parameters, below which static or dynamic momentum converges faster than restarted Lanczos with the same product budget. Numerical examples confirm the predicted crossover. The authors then alternate restarted Lanczos cycles with momentum steps, interpreting momentum as a polynomial preconditioner that damps the peaks in Lanczos's mode-wise convergence. Tests on synthetic spectra and eight SuiteSparse matrices show that the hybrid can reduce products and improve attainable residuals, especially for smaller Krylov spaces, though it is not uniformly best. Because momentum needs no orthogonalization or auxiliary projected eigenproblem, the comparison also exposes memory advantages beyond iteration counts.

### Contributions

1. Put momentum power iteration and restarted Lanczos in a common Chebyshev-polynomial convergence framework.
2. Derived spectral-gap-dependent crossover criteria for their matrix-vector-product efficiency.
3. Characterized uniform-versus-quasi-periodic damping of subdominant eigenmodes.
4. Introduced momentum-preconditioned restarted Lanczos as an alternating polynomial-filter scheme.
5. Tested the theory and hybrid method on synthetic spectra and eight sparse benchmark matrices.
