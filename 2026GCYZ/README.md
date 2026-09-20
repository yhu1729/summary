# 2026GCYZ

## ChatGPT (July 2026)

### Summary

This paper develops a second-order compact exponential time-differencing
scheme, cETD2, for three-dimensional phase-field models. The method integrates
the stiff linear differential operators exactly and approximates nonlinear
local-free-energy and elastic-interaction terms by polynomials. A carefully
chosen linear splitting controls those nonlinearities and, under explicit
parameter conditions, preserves the original discrete free-energy decay rather
than a modified energy. The authors prove the temporal convergence orders and
energy stability of the first- and second-order cETD schemes. Their parallel
software uses compact central differences, tensor contractions implemented
with DGEMM, MPI data exchange, and configurable modules for Allen--Cahn,
Cahn--Hilliard, anisotropic interfacial energy, elastic strain energy, and
boundary conditions. Numerical tests confirm the expected temporal orders and
energy decay. Large three-dimensional titanium $\beta\to\omega$ and
$\beta\to\alpha$ transformation simulations, including a $2048^3$ grid,
demonstrate long-time microstructure evolution with anisotropic interfaces and
elastic effects.

### Contributions

1. Constructed first- and second-order compact exponential time-differencing schemes for general phase-field systems.
2. Derived splitting conditions that preserve the original discrete energy-dissipation law.
3. Proved temporal convergence and error estimates for cETD1 and cETD2.
4. Implemented modular parallel software covering Allen--Cahn, Cahn--Hilliard, anisotropy, elasticity, and multiple boundary treatments.
5. Verified the method on convergent, energy-decaying titanium phase-transformation simulations up to $2048^3$ grid points.
