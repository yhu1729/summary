# 2026R2

## ChatGPT (July 2026)

### Summary

This paper develops a kernel-based quadrature algorithm for bounded smooth surfaces known only through computational nodes, a triangulation, and identified boundary nodes; neither surface nor boundary parameterizations are required. Local coordinate maps partition the surface around triangles, while radial-basis-function interpolation augmented by polynomials produces reusable weights for integrands, derivatives, normals, and surface integrals. A special boundary-sliver construction avoids exact knowledge of the boundary curve, and a stable normal approximation removes the small-node-spacing instability of earlier work. Error estimates connect convergence to polynomial reproduction and integrand smoothness. Tests on bounded rotated Cassini surfaces recover convergence orders comparable to parameterization-based predecessors; for $m=7$, the same orders are observed despite approximate geometry. Weight construction scales as $O(N)$. Accuracy degrades when nodes underresolve narrow surface regions, and unexpected parity-dependent superconvergence and more general scattered-data stabilization remain open questions.

### Contributions

1. Removed the requirement for explicit surface and boundary parameterizations.
2. Constructed local kernel-polynomial quadrature weights from triangulated surface nodes.
3. Introduced a boundary-sliver integration treatment without exact boundary curves.
4. Stabilized surface-normal approximation as node spacing decreases.
5. Established convergence estimates and observed linear weight-construction scaling.
