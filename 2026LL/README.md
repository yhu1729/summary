# 2026LL

## ChatGPT (July 2026)

### Summary

This review explains how factorization-based solvers for large sparse or compressible dense systems can remain robust on distributed CPU and GPU machines. It first frames sparse LU and multifrontal elimination through dependency DAGs and elimination trees, then examines communication- and synchronization-avoiding execution: MPI one-sided queues, three-dimensional process grids, replicated computation, and communication lower bounds. GPU sections emphasize irregular batching and fine-grained task and data parallelism. The second half surveys data-sparse formats--BLR, HSS, HODLR, $\mathcal H$, $\mathcal H^2$, butterfly, and related hierarchical factorizations--that lower arithmetic and memory complexity when off-diagonal blocks are compressible. Embedding these formats into multifrontal sparse solvers can approach linear complexity, often as a Krylov preconditioner. The chapter compares distributed packages and closes with open problems in GPU-resident preprocessing, symmetric-indefinite distributed solvers, stability, portability, and automatic compression decisions.

### Contributions

1. Gave a unified DAG and elimination-tree account of parallel supernodal and multifrontal sparse factorization and triangular solution.
2. Synthesized latency- and bandwidth-reduction techniques, including one-sided and three-dimensional communication-avoiding algorithms with explicit cost models.
3. Explained how irregular batched kernels and fine-grained scheduling expose GPU parallelism hidden by small, uneven sparse blocks.
4. Systematized hierarchical low-rank and butterfly formats, their construction and factorization, distributed layouts, and stability trade-offs.
5. Showed how structure sparsity and data sparsity combine in multifrontal solvers, surveyed distributed software, and identified major open problems.
