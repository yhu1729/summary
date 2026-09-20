# 2026VLN

## ChatGPT (July 2026)

### Summary

The paper addresses recovery of the initial velocity in a compressible anisotropic Navier--Stokes system from noisy lateral Cauchy data, assuming density, pressure, body force, and the fourth-order viscosity tensor are known. It projects the velocity onto an exponentially weighted Legendre basis in time, converting the evolutionary inverse problem into a coupled nonlinear elliptic system for spatial coefficients. An asymptotic commutation result justifies projecting the time derivative and convection nonlinearity for sufficiently regular solutions. The overdetermined elliptic system is regularized by quasi-reversibility and solved with a damped Picard iteration. Two-dimensional manufactured tests with 10% multiplicative boundary noise recover diagonal, disconnected, multiscale, and sign-changing initial structures, albeit with smoothing. Truncation acts as a temporal low-pass filter, and weighted Legendre modes markedly outperform unweighted modes. Global convergence of the nonlinear iteration in the fully anisotropic setting remains open.

### Contributions

1. Formulated an inverse initial-velocity problem for compressible anisotropic Navier--Stokes flow from lateral boundary observations.
2. Built an exponentially weighted Legendre basis suited to temporal differentiation and coefficient decay.
3. Proved asymptotic commutation of temporal projection with both the time derivative and convection nonlinearity.
4. Reduced the evolutionary problem to coupled elliptic equations solved by quasi-reversibility and damped Picard iteration.
5. Demonstrated stable reconstructions under 10% noise and quantified the benefit of exponential weighting.
