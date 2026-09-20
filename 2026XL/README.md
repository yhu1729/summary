# 2026XL

## ChatGPT (July 2026)

### Summary

This paper analyzes the spectral sign conditions underlying Van Leer and original AUSM flux-vector splittings for the one-dimensional Euler equations. By transforming between conservative variables and $(\rho,a,M)$ primitive variables, it factors the Van Leer split-flux Jacobian into one zero eigenvalue and a quadratic for the remaining pair. Explicit coefficient signs and a Sturm-sequence proof of discriminant nonnegativity establish that, for $1\leq\gamma\leq3$, $|M|<1$, and $a>0$, the two nonzero eigenvalues of $\partial F^+/\partial U$ are real and positive. This supplies the detailed proof omitted from Van Leer's original presentation; symmetry gives the corresponding negative-split result. Applying the same framework to Liou--Steffen AUSM variants reveals that linear pressure splitting violates the common-sign condition. For second-order pressure splitting, the characteristic cubic has positive coefficients, and numerical scans support a nonnegative discriminant and hence three positive real eigenvalues. The latter reality claim remains numerical rather than a complete analytic proof.

### Contributions

1. Derived explicit primitive-variable Jacobians and characteristic polynomials for Van Leer and two original AUSM pressure splittings.
2. Identified the rank deficiency that gives the Van Leer positive split one zero eigenvalue.
3. Proved discriminant nonnegativity with a Sturm sequence and established the Van Leer eigenvalue sign condition over the stated parameter domain.
4. Demonstrated analytically that AUSM with linear pressure splitting fails to keep all split-Jacobian eigenvalues of one sign.
5. Proved positive cubic coefficients for second-order AUSM pressure splitting and supplied numerical evidence that its three eigenvalues are real and positive.
