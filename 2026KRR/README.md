# 2026KRR

## ChatGPT (July 2026)

### Summary

The paper presents a scalable framework for entropy-regularized semi-discrete optimal transport from a finite-element source measure to discrete target points. Its L-BFGS dual solver accelerates dense Gibbs-kernel evaluations through adaptive, error-controlled distance truncation and R-tree neighbor queries. Coarse-to-fine hierarchies for both the source mesh and target measure provide effective initial guesses, while regularization scheduling improves convergence toward small entropy parameters. The combined strategy addresses complex geometries and PDE-derived densities without explicitly constructing Laguerre cells. Benchmarks show a 175-fold multilevel speedup in a demanding case, up to 29.5% acceleration from regularization scheduling, and 9.27-fold strong-scaling speedup on 15 nodes. Applications compute Wasserstein barycenters, register three-dimensional vascular geometries, and perform density-aware blue-noise sampling on a sphere with geodesic cost. The authors provide an open-source C++ implementation, SemiDiscreteOT, based on deal.II with hybrid MPI and OpenMP parallelism.

### Contributions

1. Developed a finite-element framework for large-scale regularized semi-discrete optimal transport.
2. Combined error-controlled kernel truncation with R-tree spatial queries.
3. Unified source and target multilevel hierarchies with regularization scheduling.
4. Demonstrated 175-fold multilevel acceleration and scalable hybrid parallel execution.
5. Validated vascular and manifold applications in an open-source deal.II implementation.
