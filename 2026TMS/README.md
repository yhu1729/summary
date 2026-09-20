# 2026TMS

## ChatGPT (July 2026)

### Summary

The paper develops prescribed-tolerance error control for rational approximations to $\mathrm{e}^{A}b$ when finite-element semidiscretization produces $A=\tau M^{-1}K$ with a well-conditioned symmetric positive-definite mass matrix $M$. Directly enclosing the numerical range $W(A)$ can be difficult and overly conservative. The authors instead use the similar matrix $\widehat A=M^{1/2}AM^{-1/2}$ and prove an error bound involving $W(\widehat A)$ and $\kappa(M)^{1/2}$. An enclosing rectangle is obtained from generalized eigenvalue problems for the symmetric and skew-symmetric parts of $K$; moreover, $W(\widehat A)$ remains in the left half-plane when $W(K)$ does. Tests use $P_1$ and $P_2$ finite elements for advection-diffusion problems on square and star-shaped domains, together with subdiagonal Pad\'e and AAA-based rational approximations. Errors meet requested tolerances in the baseline and roughly $10^4$-unknown sparse tests. Three stringent large-step AAA cases fail during scalar approximation construction, exposing an implementation limit rather than invalidating the derived bound.

### Contributions

1. Derived a numerical-range error bound for rational approximations to $\mathrm{e}^{\tau M^{-1}K}b$ through a similarity transform.
2. Reduced numerical-range enclosure to generalized eigenvalue problems involving the finite-element matrices $M$ and $K$.
3. Proved inheritance of the left-half-plane property from $W(K)$ to $W(\widehat A)$.
4. Turned the bounds into a prescribed-tolerance algorithm applicable to multiple rational approximation schemes.
5. Validated the framework on two geometries, two finite-element orders, diffusion regimes, time-step scales, and sparse matrices.
