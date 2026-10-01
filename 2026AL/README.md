# 2026AL

## ChatGPT (September 2026)

### Summary

Abgrall and Liu extend the point-average-moment polynomial-interpreted (PAMPA) method for hyperbolic conservation laws on unstructured triangles. A discontinuous Galerkin (DG) formulation followed by projection produces a globally continuous solution representation without a global mass-matrix solve, while retaining local conservation. The formulation clarifies how boundary fluxes enter updates of both interior and boundary degrees of freedom. Convex blending with low-order updates preserves admissible bounds; a rotationally invariant damping measure adds oscillation control near strong shocks. A truncation-error analysis predicts third-order accuracy for smooth solutions, which the reported convergence tests support. Numerical examples cover scalar conservation laws and compressible Euler flow. Entropy properties, error estimates, and extension beyond triangular meshes remain open in this work.

### Contributions

1. Formulated a family of PAMPA updates through DG residuals and projection onto continuous polynomials.
2. Incorporated boundary conditions consistently into residuals for interior and boundary degrees of freedom.
3. Combined bound-preserving and oscillation-eliminating parameters through convex blending.
4. Analyzed truncation error to explain third-order smooth-solution accuracy on triangular meshes.
5. Demonstrated bound preservation and shock control on scalar and Euler benchmark problems.
