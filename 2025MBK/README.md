# 2025MBK

## ChatGPT (July 2026)

### Summary

Parallel C++ algorithms can slow down when a fixed core count or chunk size is mismatched to the workload. This paper models execution time as ideal parallel work plus a measured constant overhead, then derives the work per core required to target 95% efficiency. The model is implemented in HPX as the `adaptive_core_chunk_size` execution-parameter object. On first use for an application and architecture, it measures per-iteration work and parallel overhead; subsequent calls select a bounded core count and chunk size without changing the algorithm implementation. Experiments cover the memory-bound `adjacent_difference`, a compute-bound synthetic kernel, and a ChplX `forall` loop on Intel, AMD, and RISC-V systems. Smaller inputs benefit from fewer cores, whereas larger inputs use more resources; eight chunks per core performed best in the reported sweep. The adaptive executor consistently matches the workload more effectively than fixed configurations. Memory bandwidth limits `adjacent_difference` to about $10\times$ speedup on 40 cores, while compute-bound tests reach up to $38\times$, $46\times$, and $57\times$ on 40-, 48-, and 64-core machines. The approach reduces tuning burden, although it assumes repeated invocations can amortize the initial measurements.

### Contributions

1. Derived an overhead-based model for selecting core counts at a target parallel efficiency.
2. Implemented runtime core and chunk adaptation as an HPX execution-parameter object.
3. Kept performance policy separate from parallel algorithm implementations through the executor API.
4. Evaluated memory-bound and compute-bound workloads across Intel, AMD, and RISC-V systems.
5. Demonstrated workload-dependent resource selection and near-linear speedups for the tested compute-bound kernels.
