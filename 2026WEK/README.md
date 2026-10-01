# 2026WEK

## ChatGPT (July 2026)

### Summary

The paper combines goal-oriented adaptive $h(p)$ refinement with a discontinuous Bubnov--Galerkin, NURBS-based isogeometric discretization of the first-order discrete-ordinates neutron transport equation. Dual-weighted residual estimates refine the mesh to reduce error in a prescribed quantity of interest. To accelerate scattering-dominated transport solves on the resulting irregular rational geometries, the authors derive a partially consistent diffusion synthetic acceleration scheme using a modified symmetric interior-penalty discretization. Its penalty is computed for general elements and bounded below in optically thick cells. The resulting diffusion systems are symmetric positive definite and amenable to preconditioned conjugate gradients; the same operator also preconditions GMRES. Manufactured-solution and reactor-physics benchmarks show stable compatibility with adaptive meshes, with DSA-preconditioned GMRES consistently the strongest solver considered. Scope is restricted to one-speed, isotropically scattering, fixed-source problems. High NURBS degrees can cause ill-conditioning, and diffusion solves can approach half the total runtime when standard algebraic multigrid loses effectiveness.

### Contributions

1. Combined dual-weighted-residual-driven $h(p)$ adaptivity with discontinuous Bubnov--Galerkin NURBS isogeometric neutron transport.
2. Derived a modified symmetric interior-penalty diffusion acceleration discretization.
3. Chose nonarbitrary general-element penalties with a lower bound for optically thick cells.
4. Produced symmetric-positive-definite diffusion systems usable with conjugate gradients and as GMRES preconditioners.
5. Demonstrated stable acceleration on adaptive rational-geometry reactor benchmarks.
