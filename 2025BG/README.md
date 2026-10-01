# 2025BG

## ChatGPT (July 2026)

### Summary

Distributed matrix-multiplication libraries usually dispatch among separate algorithms whose applicability depends on operand partitioning and replication. Unsupported layouts require costly redistribution. This paper instead presents one one-sided algorithm for dense $C=AB$ that accepts arbitrary one- or two-dimensional block partitionings, misaligned tiles, and replication factors. Each process uses index slicing to identify overlapping local and remote tiles, generates the required local multiplications and communications, and chooses stationary-$A$, stationary-$B$, or stationary-$C$ data movement. Operations may execute directly or be lowered to an intermediate representation whose greedy scheduler overlaps communication, multiplication, and accumulation. The C++ PGAS implementation performs direct GPU-to-GPU communication with Intel SHMEM or NVSHMEM while using vendor GEMM kernels. Tests on 12 Intel Data Center GPU Max tiles and eight NVIDIA H100 GPUs cover transformer-like matrix shapes and varied layouts. Good partitioning choices generally match or exceed PyTorch DTensor, although some H100 cases remain within about 5% of DTensor because accumulation interferes with local GEMM. Performance still depends strongly on selecting a suitable layout and stationary operand; automatic partition selection and production integration remain future work.

### Contributions

1. Introduced a single distributed dense-matrix-multiplication algorithm covering arbitrary block partitionings and replication factors.
2. Used slice-overlap arithmetic to generate local products without requiring aligned tiles or operand redistribution.
3. Unified stationary-$A$, stationary-$B$, and stationary-$C$ one-sided communication within the same implementation.
4. Added an intermediate representation and greedy schedule for overlapping GPU communication, multiplication, and accumulation.
5. Benchmarked the implementation against PyTorch DTensor on Intel and NVIDIA multi-GPU systems across transformer-derived shapes and layouts.
