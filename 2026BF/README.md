# 2026BF

## ChatGPT (July 2026)

### Summary

The paper builds first-order finite-volume schemes for weakly coupled two-dimensional systems whose flux depends on convolutions of all state variables. It approximates nonlocal terms at cell interfaces so standard monotone local fluxes, including Lax--Friedrichs- and Godunov-type choices, can be reused even though the complete nonlocal update is not monotone in every argument. Under regularity, CFL, and bounded-variation assumptions, the authors prove positivity and maximum principles, $L^1$ and bounded-variation estimates, existence and uniqueness of the weak entropy solution, convergence of the approximations, and a Kuznetsov-type $O(\sqrt{\Delta t})$ error estimate. Tests cover a scalar nonlocal model and intersecting pedestrian streams with an obstacle. At $N=800$, errors against an $N=3200$ Godunov reference are $0.801$ for the earlier Lax--Friedrichs scheme, $0.267$ for the proposed lower-viscosity variant, and $0.156$ for Godunov; only Godunov approaches first-order observed convergence. The analysis is first-order and assumption-dependent; higher-order extensions are deferred.

### Contributions

1. Reduced broad nonlocal fluxes to interface-local forms usable with monotone flux functions.
2. Established sufficient conditions for convergence to a unique weak entropy solution.
3. Proved positivity, maximum, $L^1$, bounded-variation, and time-regularity estimates.
4. Derived an $O(\sqrt{\Delta t})$ error bound for the scheme class.
5. Demonstrated reduced diffusion and near-first-order Godunov behavior in two applications.
