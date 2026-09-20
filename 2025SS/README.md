# 2025SS

## ChatGPT (July 2026)

### Summary

High-order Runge--Kutta discontinuous Galerkin schemes resolve smooth waves on unstructured meshes but generate oscillations near shocks. Conventional limiters classify cells as smooth or troubled, then retain the full polynomial or replace it with a low-order reconstruction. This paper introduces a multi-resolution limiter that instead assigns an appropriate polynomial degree. For each target cell, neighboring cell averages define a baseline smoothness indicator. The method compares this baseline successively with scaled derivatives of the DG polynomial, beginning at the highest degree. A failed comparison removes that degree's coefficients and repeats at the next degree; only repeated failure down to zero triggers a minmod TVD slope reconstruction. Thus smooth regions retain high order, derivative discontinuities receive intermediate-order polynomials, and shocks receive low-order treatment. The indicators scale identically under affine transformations of the solution, making decisions invariant to solution magnitude and offset. A fixed threshold is used across subsequent one- and two-dimensional tests on structured quadrilateral and unstructured triangular meshes. Linear-advection convergence tests recover designed orders through degree six. Euler benchmarks, including shock tubes, blast waves, double Mach reflection, sharp-corner flow, and a forward-facing step, show suppressed oscillations while retaining shock-induced structures. Its threshold still requires selection, and optimal degree-dependent values remain future work.

### Contributions

1. Introduced a multi-resolution limiter that classifies local smoothness by polynomial degree instead of making a binary good-cell / troubled-cell decision.
2. Developed a high-to-low derivative comparison that truncates only unsupported polynomial terms and invokes a minmod TVD reconstruction only after every degree fails.
3. Constructed inexpensive indicators from neighboring cell averages and local polynomial derivatives while keeping the DG reconstruction stencil compact.
4. Proved that the limiting decisions are invariant under affine rescaling and translation of the solution, improving robustness across solution scales.
5. Demonstrated designed convergence orders through degree six and non-oscillatory shock resolution for one- and two-dimensional Euler benchmarks on quadrilateral and triangular meshes using a common threshold.
