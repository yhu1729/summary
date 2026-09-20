# 2025AB

## ChatGPT (July 2026)

### Summary

Modern GPU nodes leave many CPU cores idle because applications commonly assign one MPI process to each GPU. This paper exploits those cores to accelerate large GPU-aware all-reduce operations. It partitions each GPU buffer among multiple MPI processes, shares device memory through CUDA or HIP interprocess communication where supported, and lets processes progress disjoint reductions asynchronously. The approach is combined with a node-aware multi-lane algorithm whose reduce-scatter, inter-node all-reduce, and all-gather stages reduce large off-node messages. Benchmarks cover NVIDIA A100 nodes on Delta using OpenMPI host-copy communication and AMD MI300A nodes on Tuolumne using Cray MPICH GPUDirect RDMA, including SPX, TPX, and CPX GPU partitioning modes. Large-buffer speedups reach $2.45\times$ on Delta, $1.17\times$ for the standard multi-process method on Tuolumne, and $3\times$ for multi-process multi-lane all-reduce in CPX mode. Benefits depend on topology, message size, and process count, so the method complements rather than universally replaces system collectives.

### Contributions

1. Extended node-aware multi-lane all-reduce to GPU-resident buffers with host-copy and GPUDirect RDMA communication.
2. Introduced a multiple-processes-per-GPU design using interprocess-shared buffers and asynchronous, disjoint buffer partitions.
3. Benchmarked the method on NVIDIA A100/Delta and AMD MI300A/Tuolumne against OpenMPI and Cray MPICH.
4. Showed up to $2.45\times$ large-buffer speedup on Delta and $1.17\times$ for the standard GPUDirect RDMA variant on Tuolumne.
5. Evaluated MI300A SPX, TPX, and CPX modes and obtained up to $3\times$ speedup for the multi-process multi-lane method in CPX mode.
