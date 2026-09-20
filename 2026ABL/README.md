# 2026ABL

## ChatGPT (July 2026)

### Summary

The PAMPA algorithm extends active-flux and residual-distribution ideas to hyperbolic problems on arbitrary polygonal control volumes using virtual finite element concepts. The method keeps point values on element boundaries and cell averages as degrees of freedom, but avoids explicitly constructing local polynomial bases; gradients are instead discretized from virtual-element degrees of freedom. This produces a globally continuous, formally third-order approximation with a diagonal-mass-like update structure suited to polygonal meshes. For nonlinear systems and discontinuities, the paper adds stabilization through either a MOOD-type a posteriori strategy or a monolithic convex limiter that blends high- and low-order schemes while preserving invariant-domain constraints. Numerical tests include scalar problems, acoustics, and the two-dimensional Euler equations on triangular, quadrilateral, and agglomerated polygonal meshes. The results support accuracy and robustness on complex meshes, while the authors identify higher-than-third-order extensions and mesh adaptation as future work.

### Contributions

1. Generalized active-flux-style point-average methods to arbitrary polygonal meshes through virtual finite element ideas.
2. Built the PAMPA discretization without explicit local polynomial basis functions.
3. Combined globally continuous point values with cell averages for third-order hyperbolic schemes.
4. Added MOOD and bound-preserving convex limiting strategies for shocks and invariant domains.
5. Demonstrated the method on scalar, acoustic, and Euler benchmarks over multiple mesh types.
