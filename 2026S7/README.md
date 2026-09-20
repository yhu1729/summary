# 2026S7

## ChatGPT (September 2026)

### Summary

This paper develops a full-approximation-scheme multigrid solver for elliptic problems discretized by high-order discontinuous Galerkin spectral elements on hexahedral meshes. Local $h$- and $p$-refinement uses level-specific active, twig, leaf, and frozen elements, coupling refinement zones through transfer operators without hanging nodes. The smoother employs weighted overlapping, element-centered Schwarz subdomains that include compatible face, edge, and vertex neighbors. Replacing each curved subproblem by a volume-preserving Cartesian tensor-product surrogate enables fast diagonalization with $O(p)$ work per subdomain node; an inexact Schwarz-preconditioned conjugate-gradient iteration improves robustness. Tests cover aspect ratios through 48, distorted meshes, irregular topology, and a compressor-blade geometry. Local blade refinement reduces memory by about 93% and runtime by 90% relative to global refinement, while a dynamically adapted spherical-front benchmark saves 93--98% of the degrees of freedom. Full-multigrid initialization and Hilbert-curve partitioning support parallel adaptation, and a cylinder-flow example provides a preliminary extension to incompressible Navier--Stokes problems.

### Contributions

1. Formulated a conservative DG full-approximation multigrid hierarchy for local $hp$-refinement without hanging nodes.
2. Constructed an overlapping Schwarz smoother that incorporates compatible face, edge, and vertex neighbors on irregular curvilinear meshes.
3. Combined tensor-product surrogate subproblems, fast diagonalization, and inexact Krylov acceleration for $O(p)$ work per subdomain node.
4. Demonstrated robustness to high aspect ratios, element deformation, and irregular mesh topology.
5. Quantified large memory and runtime savings from parallel dynamic adaptation and demonstrated an initial incompressible-flow application.
