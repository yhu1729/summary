# 2026BB

## ChatGPT (July 2026)

### Summary

This paper develops a distributed algorithm for one-way overset coupling between an adaptively refined forest-of-octrees mesh and an unrelated parallel mesh represented by query points. Globally replicated partition boundaries in Morton order let every process determine exact candidate owners without communication. Nonblocking point-to-point exchange then routes queries only to relevant forest processes, where a local top-down search locates leaves and evaluates application-defined data before returning results. Smooth per-tree mappings support curved multiblock domains, while opaque query objects and callbacks generalize the method beyond points. The same machinery enables refinement near mesh intersections and weighted repartitioning based on query workload. Two- and three-dimensional tests show near-linear behavior in balanced cases through 12,288 processes; a deliberately imbalanced curved-arc problem scales poorly until space-filling-curve repartitioning reduces the maximum per-process query load. An implementation in ForestClaw couples atmospheric and ionospheric solvers in a larger geophysics application. The algorithm is intrinsically one-directional, though applying it twice can couple two forest meshes.

### Contributions

1. Formulated exact, communication-free owner searches from global forest partition boundaries.
2. Combined selective nonblocking routing with local mapped-octree searches for arbitrary query sets.
3. Designed callback-based query objects that support interpolation, geometric tests, and other remote data requests.
4. Reused overset queries to drive intersection refinement and workload-aware repartitioning.
5. Demonstrated balanced scalability to 12,288 processes and integration in a multimesh geophysics simulation.
