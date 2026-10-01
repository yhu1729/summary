# 2026TK

## ChatGPT (July 2026)

### Summary

This paper develops a GPU-native clustered neighbor list for short-range particle interactions using the Hilbert space-filling-curve ordering of a Cornerstone octree. Consecutive particles form fixed-size clusters without an extra reorder, while GPU octree traversal constructs sorted cluster neighborhoods and supports particle-dependent cutoff radii. A new encoding stores interaction masks and compressed deltas between neighbor-cluster indices, reducing storage for roughly 200 neighbors to under four bytes per particle. Benchmarks on NVIDIA GH200 and AMD MI300A GPUs show neighborhood-pass performance comparable to the specialized GROMACS implementation, with hardware-dependent trade-offs between full and clustered lists. The method handles strongly nonuniform distributions and integrates naturally with octree domain decomposition and multipole long-range solvers. In a coupled smoothed-particle-hydrodynamics and gravity Evrard-collapse test, it weak-scales to 1024 GH200 GPUs and agrees with the reference solution. Cluster overhead remains significant for small neighbor counts, and pathological Hilbert-curve clusters can increase traversal and masked-interaction work.

### Contributions

1. Constructed clustered neighbor lists entirely on GPUs from an existing Hilbert-ordered octree without an additional particle reorder.
2. Designed a delta-compressed cluster-index representation requiring under four bytes per particle for approximately 200 neighbors.
3. Supported nonuniform particle distributions and particle-specific interaction radii within the same neighbor-search structure.
4. Compared construction cost, pair-kernel performance, cluster overhead, and memory use against GROMACS- and LAMMPS-style approaches on GH200 and MI300A GPUs.
5. Demonstrated coupled hydrodynamic and gravitational Evrard-collapse simulations with weak scaling to 1024 GPUs and agreement with the reference solution.
