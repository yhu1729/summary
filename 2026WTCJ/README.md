# 2026WTCJ

## ChatGPT (September 2026)

### Summary

BIT1, an electrostatic particle-in-cell Monte Carlo code with one spatial and three velocity dimensions, is modernized for heterogeneous supercomputers. The hybrid MPI+OpenMP implementation combines contiguous particle arrays, persistent device memory, pinned host memory, direct device-pointer access, and asynchronous target tasks with explicit dependencies. These changes reduce transfer and synchronization overhead while supporting NVIDIA and AMD accelerators. An ionization benchmark on four NVIDIA H100 GPUs falls from approximately 1919 to 113 seconds, a seventeenfold improvement over the initial GPU implementation. Divertor-sheath benchmarks retain 97–98% weak-scaling efficiency with minimal diagnostics through 100 nodes. With heavier diagnostics on 2000 Frontier nodes, openPMD and ADIOS2 streaming achieve 73.6% weak-scaling efficiency and a 5.25-fold strong-scaling speedup relative to 50 nodes. The study demonstrates how memory management, asynchronous execution, and scalable output jointly improve an established plasma code. Results concern the selected ionization and sheath workloads; Intel GPU support remains future work.

### Contributions

1. Implemented portable asynchronous MPI+OpenMP execution on NVIDIA and AMD GPUs using explicit task dependencies and direct device-pointer access.
2. Combined contiguous particle arrays, persistent device allocations, and pinned host memory to reduce transfer and allocation overhead.
3. Demonstrated approximately seventeenfold total-runtime improvement on four H100 GPUs through an incremental ionization-benchmark optimization study.
4. Demonstrated 97–98% weak-scaling efficiency for sheath simulations with minimal diagnostics through 100 nodes.
5. Integrated openPMD with ADIOS2 file and streaming backends, achieving 73.6% weak-scaling efficiency for simulations with heavy diagnostic output on 2000 Frontier nodes.
