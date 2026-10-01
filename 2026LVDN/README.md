# 2026LVDN

## ChatGPT (July 2026)

### Summary

This paper reconstructs an unknown initial electric field in the time-domain Maxwell system from noisy lateral Cauchy data. The method expands time dependence in a Legendre polynomial--exponential basis, converting the original three-space-plus-time inverse problem into a coupled sequence of three-dimensional spatial equations. This time splitting avoids requiring the unknown initial time derivative of the electric field. Because the available data leave the reconstruction underdetermined, the authors select a minimum-norm solution in combined space--time Sobolev norms and prove convergence under noisy measurements. Three-dimensional tests recover multiple field geometries with $10\%$ data noise, producing relative errors of about $8\%$--$16\%$. Perfectly matched layers permit longer observation intervals without boundary-reflection artifacts. A comparison with Tikhonov optimization gives similar reconstructed shapes, but the proposed approach solves one reduced linear system rather than repeatedly advancing the full four-dimensional Maxwell problem inside an outer optimization loop.

### Contributions

1. Reduced a time-dependent Maxwell initial-data inverse problem to coupled three-dimensional spatial equations.
2. Removed the need to prescribe the generally unavailable initial electric-field time derivative.
3. Defined a minimum-norm solution for the underdetermined reconstruction problem.
4. Proved convergence and stability with respect to noise-contaminated boundary measurements.
5. Demonstrated robust noisy reconstructions and lower computational structure than Tikhonov optimization.
