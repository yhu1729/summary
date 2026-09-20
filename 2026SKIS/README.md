# 2026SKIS

## ChatGPT (July 2026)

### Summary

The paper addresses conservation errors caused by child-to-parent transfer during adaptive coarsening on balanced octree meshes with continuous Galerkin finite elements. Whereas parent-to-child interpolation preserves integral quantities, standard injection discards fine-grid degrees of freedom and can accumulate mass drift over long simulations. The proposed operator first performs a local tensor-product $L^2$ restriction of fine-element quadrature values to each coarse parent, then recovers coarse nodal degrees of freedom through a global $L^2$ projection. Manufactured diffusion tests retain optimal second- and third-order convergence for linear and quadratic elements while conserving mass to numerical precision. Two- and three-dimensional Cahn--Hilliard tests, with polynomial and Flory--Huggins free energies, and a Cahn--Hilliard--Navier--Stokes rising-bubble test likewise eliminate injection-induced mass drift without disrupting energy decay. Coarsening energy mismatch falls by nearly two orders of magnitude. The implementation is communication-local before the mass solve and adds about 10% cost for Cahn--Hilliard and 7% for the coupled flow case.

### Contributions

1. Identified injection-based coarsening, rather than refinement, as the systematic conservation failure in continuous-Galerkin octree AMR.
2. Derived a dimension-independent tensor-product $L^2$ restriction followed by a global mass-matrix projection to coarse nodes.
3. Retained optimal convergence for linear and quadratic elements while reducing manufactured-solution mass drift to numerical precision.
4. Validated robust conservation and physical energy decay across Cahn--Hilliard and coupled flow problems.
5. Provided a distributed-octree implementation with communication-local restriction and measured overheads of about 10% and 7%.
