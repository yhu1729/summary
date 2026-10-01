# 2026LKCH

## ChatGPT (July 2026)

### Summary

This paper proposes an adaptive mesh refinement strategy for discontinuous Galerkin solvers of conservation laws. The method uses structured DG grids inside recursively refinable blocks, while allowing the root blocks to have unstructured connectivity represented as a forest. This combines simple local data layouts with the geometric flexibility needed for complex domains. Guard cells provide inter-block communication, and $L^2$ projection transfers solution data across nonconforming refinement interfaces so flux calculations remain local to structured block grids. Smooth boundary fidelity is maintained by projecting refined boundary nodes onto analytic surfaces or reconstructed NURBS surfaces. The FSmesh implementation includes MPI parallelism, dynamic load balancing through space-filling curves or graph partitioning, and 2D and 3D benchmark tests. Results show expected convergence for smooth problems, effective shock and vortex tracking, and good parallel efficiency. The method targets DG users who need AMR without giving up complex geometry support.

### Contributions

1. Developed a forest-of-blocks AMR structure with structured interiors and unstructured root-block topology.
2. Used guard cells and $L^2$ projection to simplify conservative DG communication across refinement levels.
3. Added analytic and NURBS-based boundary projection to preserve smooth geometry during refinement.
4. Implemented MPI load balancing with space-filling-curve and graph-partitioning options.
5. Verified convergence, dynamic refinement, and parallel performance on 2D and 3D conservation-law benchmarks.
