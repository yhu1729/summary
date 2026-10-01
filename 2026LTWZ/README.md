# 2026LTWZ

## ChatGPT (July 2026)

### Summary

The paper introduces refined implicit-explicit Runge-Kutta (R-IERK) schemes for the Cahn-Hilliard equation whose differentiation matrices and average dissipation rates do not depend on the spatial mesh or time-step size. Using discrete orthogonal convolution kernels and an updated time-space error splitting, the authors prove uniform boundedness of internal stage solutions without assuming global Lipschitz continuity of the quartic bulk nonlinearity. This permits proofs of the original, rather than modified, energy dissipation law at every stage and unconditional $L^2$ convergence. Parameterized second- and third-order schemes are constructed by optimizing average dissipation, including methods whose implicit part has an explicit first stage and need not be algebraically stable. Fourier pseudospectral experiments confirm the designed accuracy and show stable energy curves under much larger adaptive steps than comparison IERK methods, substantially reducing time levels and CPU cost.

### Contributions

1. Defined R-IERK methods with mesh- and step-independent differentiation matrices and average dissipation rates.
2. Proved uniform boundedness of all internal stages without global Lipschitz continuity of the nonlinear bulk term.
3. Established the original discrete energy dissipation law at the internal stages.
4. Proved unconditional $L^2$ convergence with full $O(\tau^p+h^m)$ accuracy under the stated positivity conditions.
5. Constructed adaptive second- and third-order schemes that use far fewer time levels than fixed-step comparisons.
