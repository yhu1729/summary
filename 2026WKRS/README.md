# 2026WKRS

## ChatGPT (September 2026)

### Summary

Willems and coauthors develop a meshless scheme for rarefied-gas flow around moving boundaries and rigid bodies. They write the Bhatnagar--Gross--Krook (BGK) kinetic equation in arbitrary Lagrangian--Eulerian form and move spatial points with the local gas velocity. Moving least squares supplies MUSCL-type spatial reconstruction on the resulting irregular point cloud; an implicit--explicit Runge--Kutta method handles transport and stiff relaxation. A multidimensional optimal-order-detection (MOOD) fallback limits oscillations near discontinuities, while a new diffuse-reflection boundary treatment avoids iterative extrapolation. Convergence studies report fourth order in one dimension and second order in two dimensions. Shock-tube, moving-plate, driven-cavity, and shear-layer tests assess discontinuities and moving geometry. Because the least-squares discretization is not strictly conservative, the paper also measures conservation errors. The demonstrations cover one- and two-dimensional, single-species gas models.

### Contributions

1. Coupled a moving-point BGK formulation to meshless MUSCL reconstruction for irregular, moving domains.
2. Combined explicit transport and implicit BGK relaxation in higher-order Runge--Kutta time integration.
3. Adapted MOOD detection to retain accuracy at smooth extrema while controlling oscillations at shocks.
4. Introduced a diffuse-reflection boundary update without iterative solution or extrapolation.
5. Quantified convergence and conservation behavior and demonstrated moving-wall and rigid-body simulations.
