# 2026D

## ChatGPT (July 2026)

### Summary

This master's thesis ports the computationally dominant kernels of TRIMEG, a Fortran particle-in-cell gyrokinetic code on triangular meshes, to GPUs with OpenMP target offloading. Particle pushing, pullback, density calculation, and grid-to-particle operations were restructured to accommodate incomplete compiler support for object-oriented Fortran and polymorphism. A unified implementation runs on AMD and NVIDIA GPUs, although compiler versions, memory models, and unified shared memory requirements limit practical portability. Kernel profiling, launch-configuration searches, single-node comparisons, and multi-node strong-scaling tests show substantial acceleration for offloaded workloads and characterize contention when multiple MPI ranks share a GPU. The hybrid MPI--OpenMP design scales across GPU nodes under suitable rank placement, but whole-application gains depend on CPU resources and remaining non-offloaded work. Correctness is checked with Cyclone and TCV-X21 ion-temperature-gradient benchmarks: GPU and CPU versions reproduce comparable field-energy growth rates and two-dimensional mode structures. The work therefore provides both an accelerated TRIMEG implementation and detailed evidence about current OpenMP-offloading constraints for complex Fortran applications.

### Contributions

1. Ported TRIMEG's particle and grid-interaction kernels to OpenMP GPU offloading.
2. Produced a common implementation for AMD and NVIDIA accelerator platforms.
3. Documented compiler failures and code transformations required for object-oriented Fortran offloading.
4. Measured kernel speedups, launch sensitivity, MPI-rank contention, and multi-node scaling.
5. Verified the accelerated code with Cyclone and TCV-X21 ion-temperature-gradient simulations.
