# 2026EAKU

## ChatGPT (July 2026)

### Summary

This paper studies performance portability in SOD2D, a Fortran spectral-element solver using OpenACC and MPI for compressible, turbulence-resolving computational fluid dynamics. The authors profile convection and diffusion kernels and explore a design space spanning FP32/FP64 arithmetic, unified or split kernels, four memory-access variants, NVIDIA V100/A100 GPUs, an AMD MI250X compute die, and weak scaling on LUMI. The same optimization does not transfer reliably across vendors, precisions, or scales. Removing explicit preloading usually beats the baseline, prefetching improves preloaded variants in selected cases, and regularizing accesses can lose performance because its auxiliary matrix is 18 times larger. Kernel splitting helps AMD in FP32 but hurts NVIDIA, with the trend reversing in FP64. At scale, the optimal channel-flow configuration changes with GPU count: applying the 32-GPU optimum at 64 GPUs can cost 23.8% throughput in FP32 and 8.3% in FP64. Small-scale or single-platform measurements are therefore inadequate predictors of multi-GPU performance, motivating architecture-, precision-, workload-, and scale-aware tuning.

### Contributions

1. Defined a performance-portability design space spanning application, memory, compiler, hardware, precision, and scale.
2. Identified convection as the dominant hotspot on both NVIDIA and AMD platforms.
3. Evaluated kernel splitting, preloading removal, cache prefetching, and regularized access on three GPU architectures.
4. Showed that optimization effects reverse across vendor and precision combinations.
5. Quantified throughput penalties from extrapolating a 32-GPU optimum to 64-GPU channel-flow simulations.
