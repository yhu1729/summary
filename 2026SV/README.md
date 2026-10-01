# 2026SV

## ChatGPT (July 2026)

### Summary

This paper analyzes an embedded Trefftz discontinuous Galerkin method for the Helmholtz equation. It begins with a polynomial DG space and imposes local PDE constraints through an embedding, avoiding explicit construction of specialized Trefftz basis functions. Global coupling uses a simple symmetric interior-penalty form rather than stronger complex or derivative stabilization. Because this formulation is noncoercive, the analysis combines $T$-coercivity with a Schatz duality argument. Under the explicit resolution condition $(1+\omega^2)h\leq C_\Omega$, it establishes wavenumber-explicit stability, quasi-optimality, optimal DG-norm convergence, and an $L^2$ estimate. Numerical experiments confirm $O(h^p)$ DG error and $O(h^{p+1})$ $L^2$ error, exponential pre-asymptotic convergence under $p$-refinement, and comparable accuracy to standard polynomial DG with fewer unknowns. High-wavenumber and spatially varying-wavenumber tests suggest useful behavior beyond the proved setting.

### Contributions

1. Formulated a polynomial embedded Trefftz DG discretization with local Helmholtz constraints and symmetric interior-penalty coupling.
2. Transferred stability to the constrained space through a $T$-coercive Schatz-type framework.
3. Proved wavenumber-explicit stability and quasi-optimality under an explicit mesh-resolution condition.
4. Derived optimal-order DG- and $L^2$-error estimates using polynomial best approximation and the Trefftz embedding.
5. Verified $h$- and $p$-convergence and explored high-frequency and variable-wavenumber regimes numerically.
