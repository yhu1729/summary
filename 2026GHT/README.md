# 2026GHT

## ChatGPT (July 2026)

### Summary

The paper develops third-order bound-preserving finite-volume methods for one-dimensional hyperbolic conservation laws on adaptive moving meshes. A high-order update is decomposed into conservative subcell updates; whenever a high-order subcell state leaves the admissible set, it is blended with a bound-preserving first-order counterpart. This produces an inexpensive flux limiter whose admissibility restriction depends only on the first-order subcell schemes. The authors also preserve the discrete geometric conservation law and prove that the limiter retains third-order spatial accuracy under a mild local CFL bound of $1/6$. The framework is extended from scalar laws to the compressible Euler equations and a nonconservative five-equation two-medium-flow model. Advection, Burgers, extreme Euler, and gas--liquid shock-tube tests show exact uniform-flow preservation, suppression of nonphysical states, and sharper resolution than comparable uniform meshes.

### Contributions

1. Derived a conservative subcell decomposition for high-order finite-volume updates on time-dependent moving meshes.
2. Converted admissibility enforcement into an inexpensive flux blend between high- and first-order subcell schemes.
3. Established bound-preserving CFL conditions that depend solely on the first-order subcell operators.
4. Proved third-order accuracy preservation under the local CFL restriction $\lambda_j\alpha\leq1/6$ while satisfying the discrete geometric conservation law.
5. Extended and validated the construction for Euler flow and the five-equation gas--liquid model, including an extreme case in which the unlimited method fails.
