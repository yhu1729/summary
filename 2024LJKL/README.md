# 2024LJKL

## ChatGPT (July 2026)

### Summary

This paper develops a GPU backend for the adaptive finite element library Gascoigne 3d, targeting geometric multigrid solvers on locally refined meshes. Rather than redesigning the discretization around GPU-specific kernels, the implementation maps existing dense and sparse linear algebra operations to cuBLAS and cuSPARSE and wraps the library's data interfaces to limit host-device transfers. Custom CUDA kernels are used only where they remove bottlenecks, such as right-hand-side assembly. The approach is tested on transport-diffusion, linear elasticity, and instationary Navier-Stokes problems, showing substantial speedups, in some cases up to about $20\times$ relative to multicore CPU runs. The experiments also identify limits: sparse matrix operations already reach high memory bandwidth, thousands of small kernel calls constrain further gains, and CPU-side matrix assembly restricts nonlinear applications. The paper argues that a conservative linear-algebra-based GPU port can deliver useful acceleration while keeping the CPU and GPU code paths maintainable.

### Contributions

1. Added GPU acceleration to an adaptive finite element multigrid code with limited code-path divergence.
2. Mapped finite element solver operations mainly to cuBLAS and cuSPARSE primitives.
3. Encapsulated data movement through custom Gascoigne 3d interface implementations.
4. Benchmarked transport-diffusion, elasticity, and Navier-Stokes examples on adaptive meshes.
5. Identified remaining bottlenecks from CPU assembly, sparse-kernel memory bandwidth, and kernel-call granularity.
