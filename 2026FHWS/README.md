# 2026FHWS

## ChatGPT (September 2026)

### Summary

The authors replace FBPIC's Numba CUDA-dependent accelerator kernels with C/C++ kernels called through CuPy RawKernel, enabling its quasi-cylindrical Fourier--Bessel particle-in-cell simulations on HIP-compatible DCUs. The Python interface, device-resident arrays, and MPI domain decomposition remain in place. Linear-wakefield and laser-wakefield-acceleration tests reproduce the original backend's field behavior, with reported relative $L^2$ field differences no greater than $5.19\times10^{-4}$. On an NVIDIA V100, the new backend is 1.32--1.54 times faster for three tested workloads. Device-specific block tuning reduces DCU step time by 24.3%. Four DCUs provide a 1.88-fold strong-scaling speedup and 2.72-fold aggregate weak-scaling throughput, about 68% efficiency; eight-DCU scaling is limited by communication and synchronization. The evidence supports portability and performance on the tested CUDA and DCU systems, with larger-cluster scaling still constrained.

### Contributions

1. Ported FBPIC's dominant particle and field kernels to a HIP-compatible CuPy RawKernel backend.
2. Preserved the existing Python workflow, device-resident data, and MPI decomposition.
3. Checked numerical agreement with the original code on wakefield benchmarks.
4. Measured single-device performance on V100 and tuned DCU thread-block configurations.
5. Profiled multi-DCU strong and weak scaling and identified inter-node communication costs.
