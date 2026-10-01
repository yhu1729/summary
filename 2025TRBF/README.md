# 2025TRBF

## ChatGPT (July 2026)

### Summary

Adaptive deterministic quadrature recursively refines subdomains according to local error estimates, creating irregular workloads that are difficult to distribute across GPUs. This paper formulates multidimensional integration as hierarchical domain decomposition: each MPI rank owns one GPU and independently advances a collection of subregions using a Genz--Malik cubature rule. A decentralized cyclic round-robin policy periodically moves bounded batches of subregions between ranks through nonblocking, CUDA-aware MPI communication that partially overlaps evaluation. On one GPU, the method is competitive with the PAGANI package and is more robust for oscillatory and discontinuous integrands at tight tolerances. Distributing memory makes cases through dimension 11 feasible and produces speedups of up to an order of magnitude over PAGANI in the reported tests. Strong scaling is limited: performance generally improves from two to four GPUs but can flatten or regress at eight and twelve because global convergence checks, slowly propagated imbalance, and unfinished communication create idle time. The study therefore demonstrates that multi-GPU adaptivity extends the attainable dimension and accuracy, while showing that better initial partitioning and more informed load redistribution are needed for scalable efficiency.

### Contributions

1. Cast adaptive multidimensional quadrature as a distributed hierarchical domain-decomposition problem for multi-GPU systems.
2. Designed decentralized cyclic load redistribution using bounded, nonblocking CUDA-aware MPI transfers.
3. Improved robustness over PAGANI for difficult oscillatory and discontinuous integrands at tight tolerances.
4. Extended deterministic adaptive integration to reported cases as high as dimension 11 with up to order-of-magnitude speedups.
5. Quantified the synchronization, load-imbalance, and communication bottlenecks that limit strong scaling beyond four GPUs.
