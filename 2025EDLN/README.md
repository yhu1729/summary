# 2025EDLN

## ChatGPT (July 2026)

### Summary

Unstructured discrete-ordinates transport sweeps form a directed acyclic graph whose wavefront widths and finite-element solve times vary, causing load imbalance at bulk-synchronous barriers. After benchmarking the existing UnSNAP mini-application across current CPUs and GPUs, this work replaces its shared-memory bucket schedule with recursive OpenMP tasks. One initial task per angle processes all energy groups for an element; atomic dependency counters release downwind elements when their final upwind prerequisite completes. Work-first generation limits the number of live tasks, while distributed task queues, affinity, and work stealing improve locality and balance. On $16^3$-element synthetic meshes, the asynchronous many-task implementation matches or outperforms the bulk-synchronous version in almost every tested angle, group, and finite-element-order configuration on AMD Genoa, Intel Sapphire Rapids, and NVIDIA Grace CPUs. Gains reach roughly $2.4\times$ and are strongest at first order; they diminish as higher-order element work dominates scheduling overhead. On Sapphire Rapids, synchronization-wait cycles fall from 33.58% to 9.45% for first-order tests. The evaluation preserves integrated-flux results within floating-point reordering effects. Scope remains single-node CPU execution with parallel-block-Jacobi communication; GPU tasking and other distributed-memory sweep schemes are future work.

### Contributions

1. Updated the performance characterization of UnSNAP's bulk-synchronous transport sweep on modern many-core CPUs and GPUs.
2. Designed a recursive work-first task algorithm that respects unstructured sweep dependencies through atomic counters.
3. Combined angle-level concurrency with distributed task queues, affinity, and work stealing to reduce imbalance and synchronization.
4. Demonstrated up to roughly $2.4\times$ speedup across three CPU architectures while preserving the numerical result.
5. Attributed performance gains to sharply reduced synchronization waiting and quantified their decline as finite-element order increases.
