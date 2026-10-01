# 2026LTTS

## ChatGPT (July 2026)

### Summary

This study reviews and benchmarks open-source quadrature software for finite elements cut by implicitly or explicitly represented boundaries. A common MATLAB interface exercises Algoim, BoSSS, FCMLab, Gridap, mlhp, ngsxfem, Nutils, QuESo, and related tools on two- and three-dimensional domain integrals, using matched geometries and polynomial test functions to compare accuracy, efficiency, robustness, and sensitivity to requested quadrature order. All tested codes are usable and robust for the selected cases, but their error--cost behavior differs substantially. Tessellation-based approaches introduce geometry approximation error that commonly limits convergence to second order; methods preserving curved boundaries or higher-order approximations can attain higher-order convergence. Increasing the nominal quadrature order does not necessarily reduce error when geometric approximation dominates, so total quadrature-point count is a more informative cost measure than an input order alone. The accompanying test environment and reusable quadrature-point outputs support reproducible comparisons. The review also identifies a missing open-source capability: volume quadrature for parametric boundary representations needed in CAD-based workflows.

### Contributions

1. Cataloged open-source cut-element quadrature implementations and classified their boundary-representation strategies.
2. Built reproducible two- and three-dimensional benchmarks with both implicit and explicit geometry descriptions.
3. Compared accuracy against total quadrature-point cost rather than relying only on nominal integration order.
4. Demonstrated how tessellated geometry errors cap convergence while higher-order boundary representations permit higher accuracy.
5. Released a common MATLAB test interface and identified parametric-boundary volume quadrature as an unresolved software gap.
