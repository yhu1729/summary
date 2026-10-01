# 2025GRD

## ChatGPT (July 2026)

### Summary

The paper develops cell-centered finite-volume schemes with genuinely multidimensional nodal fluxes on unstructured polygonal Voronoi-like meshes. One solver extends Osher--Solomon dissipation by integrating absolute flux Jacobians over a dual simplex and returns the full multidimensional flux tensor. A second reformulates residual-distribution fluctuations as corner fluxes and instantiates them with Roe's multidimensional N scheme. Both are complete because they use the hyperbolic system's full eigenstructure. CWENO reconstruction and one-step ADER time discretization provide orders up to four in space and time. Compressible-Euler tests verify designed convergence and show sharper contacts and shear structures than conventional edge-normal solvers. The multidimensional Osher solver strongly suppresses carbuncle behavior without an added fix; the N-based method with its standard shock fix remains carbuncle-free and comparatively low-dissipation. Some low-dissipation tests exhibit reduced angular symmetry or boundary instabilities.

### Contributions

1. Provided a corner-flux framework for complete multidimensional Riemann solvers on polygonal meshes.
2. Constructed an Osher-type solver computing an entire flux tensor through dual-simplex Jacobian integration.
3. Related finite-volume corner-flux fluctuations to residual-distribution schemes.
4. Converted the multidimensional N-scheme fluctuation into a practical finite-volume nodal flux.
5. Built high-order CWENO--ADER variants and demonstrated convergence, low dissipation, and carbuncle resistance.
