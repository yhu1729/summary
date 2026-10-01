# 2025C

## ChatGPT (July 2026)

### Summary

HYLU is a sparse direct solver for shared-memory multicore systems that adapts its numerical factorization to the matrix's sparsity pattern. Rather than relying uniformly on supernodes and Level-3 BLAS, it combines row-row, supernode-row, and supernode-supernode update kernels, then selects among them using symbolic information such as predicted work and supernode structure. Preprocessing applies matching and scaling, fill-reducing ordering, and symbolic factorization. Numerical factorization uses a dependency graph with bulk parallelism in wide levels and pipelined execution along dependency chains. On 37 SuiteSparse matrices, HYLU's factorization was geometrically 2.36 times faster than Intel MKL PARDISO for one-time solves and 2.90 times faster for repeated solves. For repeated solves, factorization plus substitution was faster on every tested matrix, with a 2.53-fold geometric-mean speedup. The reported residuals were also smaller on average, although both solvers struggled with an extremely ill-conditioned case. The results support hybrid kernel selection as an alternative to applying dense-block kernels indiscriminately across sparse problems.

### Contributions

1. Developed a general-purpose sparse LU solver that adapts to matrices with widely differing sparsity patterns.
2. Unified row-row, supernode-row, and supernode-supernode updates in one factorization data structure.
3. Selected numerical kernels from symbolic sparsity and work estimates instead of using a fixed supernodal strategy.
4. Combined level-based bulk parallelism with pipelined execution along strong dependency chains.
5. Demonstrated substantial factorization and repeated-solve speedups over Intel MKL PARDISO on 37 SuiteSparse matrices.
