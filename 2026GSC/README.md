# 2026GSC

## ChatGPT (July 2026)

### Summary

This work extends conservative Lagrange-Galerkin convection schemes to quadratic finite elements, where characteristic transport curves element sides and invalidates straight-element intersection formulas. It develops three supermesh algorithms: Single Straight-sided Triangles (SST), Division in Straight-sided Triangles (DST), and Division in Curved Triangles (DCT). These compute transported-mesh integrals to machine accuracy, restoring mass conservation and unconditional time-step stability. Numerical tests on uniform and adaptively refined meshes show DCT retains projection-like $L^2$ accuracy while reducing mass error by as much as ten orders of magnitude; SST and DST match this on uniform grids but can lose accuracy under local refinement. DCT is best for very low-error refined solutions, DST for intermediate errors, and SST when larger errors are acceptable. A dynamic side-correction criterion reduces the added supermesh cost, and all intersection operations are element-local and readily parallelizable.

### Contributions

1. Extended conservative Lagrange-Galerkin mesh intersection to transported quadratic curved elements.
2. Formulated SST, DST, and genuinely curved DCT supermesh algorithms.
3. Achieved machine-precision transported integrals, mass conservation, and stability without a CFL restriction.
4. Established accuracy-cost regimes and up to ten orders of mass-error improvement on uniform and adaptive meshes.
5. Introduced a dynamic correction-selection criterion and identified elementwise parallelism.
