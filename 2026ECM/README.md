# 2026ECM

## ChatGPT (September 2026)

### Summary

NektarIR is a domain-specific compiler for high-order spectral/$hp$ finite-element operators used in computational fluid dynamics. Its custom MLIR dialect represents elemental operations and records element shape, basis or quadrature, and data layout before lowering the operations through reusable MLIR dialects to CPU or GPU code. The paper implements sum-factorized Helmholtz kernels on three-dimensional hexahedral and tetrahedral elements. CPU code vectorizes across elements; GPU code explores one thread per element and one thread per expansion coefficient. Benchmarks against hand-written Nektar++ kernels show higher throughput for NektarIR on the tested AMD EPYC CPUs, but lower throughput on the NVIDIA H100 for large problems, particularly for coefficient-threaded tetrahedral kernels. Measured generation and compilation overhead is under one second for the tested kernels. The work demonstrates a route to generating hardware-specific kernels from one operator description while identifying GPU register pressure and other performance gaps as remaining work.

### Contributions

1. Defined an MLIR dialect whose block type records element shape, expansion or quadrature data, and memory layout for spectral/$hp$ operators.
2. Lowered composed Helmholtz operations to fused, sum-factorized elemental kernels through domain-specific transformations and standard MLIR dialects.
3. Implemented CPU vectorization across elements and two GPU threading strategies, including loop coalescing for triangular and tetrahedral iteration spaces.
4. Measured sub-second kernel lowering and just-in-time compilation on the tested CPU and GPU configurations.
5. Compared generated and hand-written Nektar++ Helmholtz kernels, finding higher CPU throughput but unresolved GPU performance deficits.
