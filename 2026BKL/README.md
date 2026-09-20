# 2026BKL

## ChatGPT (July 2026)

### Summary

This paper develops a compact, implicit form of the local anisotropic basis function method (LABFM) for high-order meshless differentiation on irregular point clouds. Lele-type implicit stencils are selected locally, and their coefficients are optimized over two-dimensional wavenumber space to improve resolving power while encouraging diagonal dominance and a well-conditioned global sparse system. Second- and fourth-order gradient and Laplacian operators resolve substantially more of the admissible spectrum than explicit LABFM; some fourth-order Laplacians exhibit spectral-like behavior. Convergence tests confirm lower differentiation errors, although compact gradient operators remain unstable for purely advective problems and may require filtering. In viscous Burgers simulations, compact schemes reduce early, advection-dominated errors by as much as an order of magnitude. For Poisson problems on a domain with a curved internal boundary, the largest compact stencils also reduce error by about an order of magnitude with nearly no additional solve cost. The study is a proof of concept, and coefficient forms and stencil selection remain open optimization questions.

### Contributions

1. Formulated compact LABFM operators using local implicit Lele-type stencils on unstructured node sets.
2. Designed a coefficient-selection procedure that balances wavenumber resolution, diagonal dominance, and conditioning.
3. Quantified spectral-like resolving behavior for second- and fourth-order gradient and Laplacian operators.
4. Established convergence and stability characteristics, including the remaining instability of compact advection operators.
5. Demonstrated up to order-of-magnitude error reductions for viscous Burgers and curved-domain Poisson problems.
