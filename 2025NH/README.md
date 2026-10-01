# 2025NH

## ChatGPT (July 2026)

### Summary

Nonlocal traffic models let vehicle speed depend on an averaged downstream density, but numerical schemes can lose stability as the interaction horizon $\varepsilon$ shrinks toward the local Lighthill--Whitham--Richards conservation law. The paper analyzes a Godunov-type finite-volume discretization with mesh size $h$, focusing on the convolved density $W_{\varepsilon,h}$ rather than the possibly variation-growing density $\rho_{\varepsilon,h}$. For convex, anisotropic kernels and normalized quadrature weights, a refined argument proves a maximum principle and uniform total-variation-diminishing estimates. A new nonlocal entropy condition yields a discrete Kružkov inequality compatible with the local entropy condition. Compactness and Kuznetsov's method then show that $W_{\varepsilon,h}$ converges along arbitrary joint limits $\varepsilon,h\to0$ to the unique entropy solution, with $L^1$ error bounded at order $\varepsilon+h+\sqrt{\varepsilon t}+\sqrt{h t}$. For the exponential kernel, an $L^1$ deviation estimate transfers convergence to $\rho_{\varepsilon,h}$, while the continuous convolved density satisfies an $L^1$ contraction property. Numerical experiments with shocks, rarefactions, smooth data, several kernels, velocity laws, and limiting paths support the theory. They also show that quadrature normalization is essential: unnormalized weights can cause persistent error, whereas normalized weights recover convergence. Results beyond the hypotheses suggest extensions to constant kernels and broader density convergence. This supplies a robust scheme across both nonlocal and local modeling regimes.

### Contributions

1. Proved asymptotic compatibility of a Godunov-type scheme for bounded-variation initial data, general convex downstream kernels, and nonlinear velocity laws, without requiring density to remain bounded away from zero.
2. Established a maximum principle and uniform total-variation-diminishing bounds for the discretized convolved density by exploiting kernel convexity.
3. Introduced a nonlocal entropy condition and a compatible discrete Kružkov inequality that ensure entropy admissibility in the local limit.
4. Derived the explicit $L^1$ convergence rate $O(\varepsilon+h+\sqrt{\varepsilon t}+\sqrt{h t})$ along arbitrary joint limits of the horizon and mesh parameters.
5. For exponential kernels, extended convergence to the discretized traffic density and proved an $L^1$ contraction property for the continuous convolved density.
