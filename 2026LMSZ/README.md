# 2026LMSZ

## ChatGPT (July 2026)

### Summary

The paper constructs optimization-based postprocessors that keep high-order gas-dynamics solutions inside the convex invariant domain of positive density and internal energy while retaining global conservation. An explicit projection onto the admissible Euler-state set enables Davis--Yin splitting for the $\ell_2$ limiter; Douglas--Rachford splitting, with an inner Davis--Yin solve, handles the $\ell_1$ limiter. In discontinuous Galerkin schemes, the optimization first repairs cell averages and a Zhang--Shu scaling limiter then repairs quadrature values. Manufactured tests retain optimal high-order convergence. Sedov blast-wave and Mach-2000 astrophysical-jet tests remain robust, locate shocks correctly, and work with both strong-stability-preserving and non-strong-stability-preserving Runge--Kutta schemes. The $\ell_2$ method is generally cheaper, whereas the $\ell_1$ limiter is activated less often in the jet test. The approach preserves global, but not cell-local, conservation.

### Contributions

1. Derived an efficient explicit projection onto the gas-dynamics invariant domain.
2. Formulated a Davis--Yin $\ell_2$ invariant-domain limiter.
3. Formulated a nested Douglas--Rachford/Davis--Yin $\ell_1$ limiter.
4. Combined cell-average optimization with Zhang--Shu pointwise scaling for high-order discontinuous Galerkin methods.
5. Verified accuracy and robustness on manufactured solutions, Sedov blast waves, and Mach-2000 jets.
