# 2026HVFO

## ChatGPT (July 2026)

### Summary

This paper extends Chebyshev-polynomial time propagation from Hermitian Hamiltonians with spectra in $[-1,1]$ to arbitrary non-Hermitian matrices with complex spectra. Because the Chebyshev series for the exponential converges over the whole complex plane, the restriction is numerical rather than analytic. Outside $[-1,1]$, Chebyshev polynomials grow exponentially, so cancellation with decreasing Bessel coefficients exposes floating-point rounding error. Using Bernstein ellipses, the authors derive a large-$t\rho$ bound, $\widetilde{\Delta}<2\epsilon t\rho\exp(t\rho/2)$, and invert it to obtain a safe spectral radius for a prescribed tolerance and time step. A Jordan-form argument extends the expansion to diagonalizable and nondiagonalizable square matrices, while a matrix-vector recurrence avoids forming the propagator. Simulations of Gaussian wave packets in the Hatano-Nelson model under periodic and open boundaries agree with analytic evolution when the step size is chosen from the spectral geometry. Stable non-unitary propagation is therefore achievable by reducing the time step as the enclosing Bernstein ellipse grows.

### Contributions

1. Extended the Chebyshev expansion of the exponential to arbitrary non-Hermitian square matrices.
2. Identified floating-point rounding as the practical limitation outside the conventional spectral interval.
3. Derived a rounding-error bound using the Bernstein ellipse enclosing the complex spectrum.
4. Provided a tolerance criterion for choosing a safe spectral radius or time step.
5. Validated matrix-vector propagation on the Hatano-Nelson model for open and periodic boundaries.
