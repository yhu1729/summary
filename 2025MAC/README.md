# 2025MAC

## ChatGPT (July 2026)

### Summary

Malleable MPI applications can return or acquire resources while running, but process creation and communicator layout make resizing expensive. Existing approaches either respawn the full application or retain processes that prevent entire nodes from being released. This paper introduces two cooperative spawning strategies in which active and newly created processes participate in parallel process creation before data redistribution. The Hypercube strategy targets homogeneous allocations; Iterative Diffusive spawning also supports allocations with different core counts per node. Both arrange each MPI_COMM_WORLD-derived communicator within a node, enabling fast shrinking by terminating surplus processes instead of leaving zombie ranks or spawning replacements. The methods are integrated into the MaM malleability library and evaluated on two systems. Expansion remains competitive, with worst-case overheads of $1.13\times$ for homogeneous and $1.25\times$ for heterogeneous allocations. Shrinking is at least $1387\times$ and $20\times$ faster in the corresponding scenarios. Heterogeneous hardware load balancing and further synchronization reductions are left open.

### Contributions

1. Designed a parallel MPI spawning algorithm for malleable applications on homogeneous allocations.
2. Extended the strategy to allocations with heterogeneous numbers of cores per node.
3. Enabled shrink operations to terminate surplus ranks and release complete nodes without respawning the application.
4. Integrated the new resizing paths into the MaM library while preserving existing processes.
5. Demonstrated competitive expansion and orders-of-magnitude faster shrinking on two systems.
