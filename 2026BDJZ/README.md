# 2026BDJZ

## ChatGPT (July 2026)

### Summary

The paper treats equilibrium-phase discovery in the Landau--Brazovskii model as computation of second-order stationary points, thereby distinguishing local minima from saddle points that can trap energy-decreasing first-order schemes. After Fourier pseudospectral discretization, the authors introduce an implicit--explicit trust-region method whose outer iteration is proved to approach second-order stationarity. Its nonconvex trust-region subproblem is solved globally by exploiting complementary Hessian structure: the interaction operator is diagonal in reciprocal space, while the nonlinear bulk term is diagonal in physical space, enabling FFT-based operations. Numerical comparisons with Bregman proximal-gradient, semi-implicit, SAV, IEQ, and exponential-time-differencing methods show that first-order methods can retain negative Hessian eigenvalues, whereas IMEX-TR reaches nonnegative curvature. The method also escapes converged saddles when applied as post-processing. It discovers cubic FDDD as a stable Landau--Brazovskii phase and maps a previously missing thermodynamic stability region without altering established neighboring regions.

### Contributions

1. Reframed stable Landau--Brazovskii phase computation around second-order rather than merely first-order stationarity.
2. Introduced IMEX-TR and proved convergence of its outer iteration to second-order stationary points.
3. Provided a globally convergent trust-region subproblem solver using negative curvature and FFT-exploitable Hessian structure.
4. Showed that IMEX-TR avoids or escapes saddles where representative first-order methods stagnate.
5. Identified the cubic FDDD phase as stable and added its stability region to the model's phase diagram.
