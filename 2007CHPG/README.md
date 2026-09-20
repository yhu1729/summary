# 2007CHPG

## ChatGPT (August 2026)

### Summary

This paper develops a unified design framework for MPI collective communication on distributed-memory machines. Using a latency--bandwidth--computation model with message cost $\alpha+n\beta$ and reduction cost $\gamma$, it derives lower bounds for broadcast, reduce, scatter, gather, allgather, reduce-scatter, and allreduce. It presents dual families of minimum-spanning-tree, recursive-doubling or halving, bidirectional-exchange, bucket, and simple algorithms for linear arrays, multidimensional meshes, hypercubes, and fully connected networks. Short messages favor latency-minimizing tree algorithms; long messages favor bandwidth-efficient composed algorithms. For intermediate sizes, the authors organize algorithms into parameterized hybrids obtained by factoring processors into logical mesh dimensions and choosing kernels per dimension. They prove a restricted optimality result for hypercubes and derive a practical heuristic for arbitrary factorizations. MPI point-to-point implementations in the InterCol library are benchmarked on a Myrinet-connected Cray-Dell cluster; broadcast and reduce-scatter trends largely match the model and are often competitive with or faster than the tested MPICH-GM collectives. The model and measurements assume a uniform, historical cluster architecture, so performance rankings do not directly generalize to modern systems.

### Contributions

1. Derived latency, bandwidth, and computation lower bounds for seven principal collective communication operations under one cost model.
2. Presented collective algorithms as dual, reusable families, including tree, exchange, doubling or halving, and bucket constructions.
3. Generalized one-dimensional algorithms systematically to meshes, hypercubes, and logically fully connected architectures.
4. Constructed parameterized hybrids for intermediate messages, proved restricted hypercube optimality, and proposed a factorization-based heuristic for general processor counts.
5. Implemented the designs with MPI point-to-point operations and compared broadcast and reduce-scatter results with the model and MPICH-GM.
