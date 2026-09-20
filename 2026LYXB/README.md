# 2026LYXB

## Codex/ChatGPT (September 2026)

### Summary

This paper accelerates collisionless local linear gyrokinetic eigenanalysis by
using particle energy and magnetic moment as velocity-space coordinates.
Passing and trapped trajectories then form independent one-dimensional orbit
blocks coupled only through the field equations. The MGK solver discretizes
passing orbits with Legendre--Gauss--Lobatto differentiation, trapped orbits in
a periodic bounce-angle representation, and separates quadrature at the
trapped--passing boundary. A Schur-complement shift-invert Arnoldi method avoids
factoring the full generalized eigenproblem and reduces per-shift scaling from
cubic to linear in the number of orbit blocks. Batched GPU operations extend
the method to kinetic electrons, Miller geometry, and electrostatic or
electromagnetic two- and three-field models. ITG, TEM, and KBM frequencies and
eigenfunctions generally agree with CGYRO and other reference solvers within a
few percent. Reported solves take roughly $0.01$--$0.1$ seconds on a GPU and can
be over three orders of magnitude faster than CGYRO. The demonstrated scope is
local, linear, and collisionless; nonlinear and transport extensions remain
future work.

### Contributions

1. Decomposed collisionless gyrokinetic dynamics into orbit-invariant passing and trapped blocks.
2. Combined orbit-specific spectral discretizations with separatrix-aware velocity-space quadrature.
3. Derived a Schur-complement shift-invert eigensolver whose cost is linear in the number of orbit blocks.
4. Extended MGK to kinetic electrons, Miller geometry, and two- and three-field electromagnetic models.
5. Validated mode spectra and eigenfunctions while demonstrating sub-second GPU solutions.
