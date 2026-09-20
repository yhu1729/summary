# 2026LQ

## ChatGPT (July 2026)

### Summary

The spectral-volume method obtains a high-order polynomial in each spectral volume from control-volume averages, but discontinuities require limiting to suppress spurious oscillations. This paper develops a control-volume simple WENO limiter that combines the original high-order reconstruction with linear polynomials formed from a target control volume and its neighbors using nonlinear weights. The limited polynomial may be discontinuous inside a spectral volume, so numerical fluxes are used at troubled-control-volume and spectral-volume boundaries, while direct physical-flux evaluation remains possible where the reconstructed solution is continuous. The construction uses only a few linear candidate polynomials, preserves the compact stencil of the spectral-volume method, and retains control-volume resolution. Tests on one- and two-dimensional scalar conservation laws and Euler systems recover the designed convergence rates for smooth solutions and resolve shocks, blast waves, Riemann problems, a forward-facing step, and double-Mach reflection without unstable oscillations.

### Contributions

1. Introduced a control-volume-based simple WENO limiter for the spectral-volume method.
2. Combined the original high-order reconstruction with local linear candidates through nonlinear weights.
3. Supplied consistent numerical-flux treatment for newly discontinuous internal control-volume interfaces.
4. Preserved compactness and control-volume resolution with a small set of simple candidate polynomials.
5. Demonstrated high-order accuracy and robust shock resolution on one- and two-dimensional scalar and system tests.
