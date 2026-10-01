# 2026LZG

## ChatGPT (July 2026)

### Summary

This paper develops a quadrature method for uniformly sampled, nonperiodic integrands using local Fourier extensions. Each overlapping window is continued onto a larger periodic interval through a truncated-SVD-stabilized Fourier fit, and its integral is evaluated analytically from the Fourier coefficients. Uniform windows share the same discrete fitting matrix, so its factorization is precomputed once and reused in an offline/online implementation. The authors bound the quadrature error by the local approximation error and derive algebraic convergence for Sobolev-regular functions. Tests on smooth, oscillatory, and spatially varying-frequency functions reach near machine precision with fewer samples than composite Simpson quadrature. For continuous piecewise-smooth functions, coefficient-energy outliers identify suspect windows; a local procedure brackets the singular point, predicts one-sided values, and replaces only the affected contribution, restoring near-spectral accuracy in the reported cases. Jump discontinuities, multidimensional extensions, and a rigorous adaptive-refinement strategy remain open.

### Contributions

1. Converted stabilized local Fourier extensions into an analytic quadrature rule on uniform samples.
2. Reused a precomputed truncated-SVD factorization across identical local windows.
3. Bounded integration error through local approximation error and established Sobolev convergence rates.
4. Developed coefficient-energy detection and localized correction for derivative singularities.
5. Demonstrated near-machine or near-spectral accuracy on smooth, oscillatory, and piecewise-smooth tests.
