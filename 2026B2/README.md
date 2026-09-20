# 2026B2

## ChatGPT (July 2026)

### Summary

This review connects linear Boltzmann transport across radiative transfer, neutron transport, and rarefied-gas dynamics through the Analytical Discrete Ordinates (ADO) method. Angular quadrature converts the integro-differential transport equation into coupled first-order equations; ADO solves their homogeneous part through a reduced-order eigensystem and supplies explicit spatial dependence useful for accurate direct and inverse calculations. The article develops the slab problem, general boundary conditions, anisotropic scattering, and particular solutions, then shows how transverse integration and nodal balance extend the construction to two-dimensional Cartesian geometry. It surveys tailored quadratures, including Legendre--Chebyshev product rules, and reports that ADO nodal schemes can outperform comparison methods on coarse meshes while supporting spatial and angular error studies. Applications include reactor shielding and multiplication factors, radiative transfer, source or coefficient reconstruction, and kinetic models for microflows. The review closes by identifying large linear systems, joint spatial-angular error analysis, and multidimensional optical-tomography inversion as open directions rather than presenting ADO as a finished universal solver.

### Contributions

1. Unified photon, neutron, and rarefied-gas linear Boltzmann models under a common discrete-ordinates viewpoint.
2. Derived the one-dimensional ADO solution using half-range quadrature and a reduced-order eigenvalue problem with general boundary and particular solutions.
3. Extended ADO to two-dimensional Cartesian transport through transverse integration and an analytical nodal formulation.
4. Synthesized quadrature design and error studies, including product quadratures and Richardson-based spatial convergence estimates.
5. Connected explicit ADO spatial formulas to shielding, criticality, inverse transport, and linearized-Boltzmann kinetic problems while identifying concrete open problems.
