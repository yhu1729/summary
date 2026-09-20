# 2026KSKB

## ChatGPT (July 2026)

### Summary

This work extends entropy-stable discontinuous Galerkin spectral-element methods to arbitrary-order curvilinear hybrid meshes containing quadrilaterals and triangles in two dimensions and hexahedra, prisms, tetrahedra, and pyramids in three. Collapsed-coordinate tensor products retain sum-factorization efficiency; Legendre--Gauss collocation, generalized summation-by-parts operators, entropy projection, and two-point fluxes yield free-stream-preserving entropy-conservative or entropy-stable hyperbolic discretizations. A lifting formulation handles viscous terms. To avoid the severe explicit time-step restriction associated with collapsed nodal coordinates, the method evolves modal degrees of freedom and applies a memory-efficient weight-adjusted inverse mass matrix. Analyses and experiments establish free-stream preservation, grid and polynomial convergence, and entropy behavior on hybrid curvilinear meshes. Taylor--Green vortex, NACA 0012, and NASA Common Research Model simulations demonstrate application-scale compressible-flow capability. The entropy proof is restricted to the hyperbolic operator, curved-pyramid convergence is not guaranteed, and the Common Research Model test does not resolve the boundary layer.

### Contributions

1. Constructed an arbitrary-order entropy-stable DG spectral-element method for curvilinear meshes mixing all standard two- and three-dimensional element shapes.
2. Used collapsed-coordinate tensor products to retain sum-factorization structure instead of dense multidimensional summation-by-parts costs.
3. Combined Legendre--Gauss collocation, generalized summation by parts, entropy projection, and two-point fluxes to establish free-stream and hyperbolic entropy properties.
4. Evolved modal unknowns with a weight-adjusted inverse mass approximation to alleviate collapsed-grid time-step restrictions.
5. Validated convergence and entropy behavior and demonstrated NACA 0012 and 216,718-element NASA Common Research Model simulations.
