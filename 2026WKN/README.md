# 2026WKN

## ChatGPT (July 2026)

### Summary

The paper constructs nonlinear numerical boundary fluxes for open-boundary hyperbolic problems whose entropy or energy growth is provably bounded only by prescribed exterior data. It rewrites the entropy flux as a quadratic form in nonlinear characteristic variables and derives an algebraic compatibility condition between a characteristic penalty and the numerical flux. The framework applies directly to split-form discontinuous Galerkin spectral element and related summation-by-parts discretizations. Explicit fluxes are obtained for Burgers' equation and for every subcritical or supercritical inflow/outflow regime of the two-dimensional shallow-water equations; because physical energy is an entropy for these systems, the bounds also establish energy stability. Manufactured-flow tests verify accuracy, while a geostrophic-adjustment experiment shows that the new outflow flux damps reflections and runs to completion. Standard linearly derived LLF and HLL boundary treatments crash near $t=19.5$ unless extra interior dissipation is introduced.

### Contributions

1. Proved a general algebraic condition ensuring that a nonlinear boundary flux bounds the discrete entropy rate solely by external data.
2. Connected nonlinear characteristic SAT penalties to numerical boundary-flux construction for split-form SBP/DGSEM schemes.
3. Derived an energy-stable Burgers inflow flux and showed why common entropy-conservative and LLF choices lack the required data-only bound.
4. Constructed explicit shallow-water fluxes for all four subcritical and supercritical inflow and outflow regimes.
5. Demonstrated accurate, robust open-boundary behavior where conventional linearly derived LLF and HLL boundary treatments fail.
