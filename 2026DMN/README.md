# 2026DMN

## Codex/ChatGPT (September 2026)

### Summary

This paper develops high-order summation-by-parts finite differences for the
two-dimensional, two-velocity Vlasov--Maxwell system. Tensor-product operators
retain the one-dimensional SBP structure, while a Lax--Friedrichs split
upwind operator suppresses filamentation instabilities that destabilize the
central scheme. The semidiscrete method conserves mass and momentum,
propagates Gauss's law, and makes the distribution's discrete $L^2$ norm
nonincreasing; exact energy conservation applies to the central variant, while
upwinding adds controlled dissipation. A matrix-free CUDA implementation stores
only local stencil coefficients, flattens the four-dimensional distribution,
and uses atomic moment accumulation instead of assembled global matrices.
Manufactured solutions recover second-, fourth-, and sixth-order convergence.
Diocotron, Weibel, and two-species Kelvin--Helmholtz simulations demonstrate
the method on a single NVIDIA L40 GPU, including a reported case with about 420
million degrees of freedom. Strong magnetic fields remain costly under the
explicit time integrator, and extending the approach to 3D3V will require
implicit treatment and multi-GPU decomposition.

### Contributions

1. Constructed tensor-product SBP discretizations for the 2D2V Vlasov--Maxwell equations.
2. Introduced split upwind stabilization with provable mass, momentum, Gauss-law, and norm properties.
3. Implemented the scheme as matrix-free CUDA kernels without assembled multidimensional operators.
4. Verified second-, fourth-, and sixth-order accuracy using manufactured solutions.
5. Demonstrated large single-GPU diocotron, Weibel, and Kelvin--Helmholtz simulations and documented scaling limits.
