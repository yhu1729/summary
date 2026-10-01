# 2025WMKK

## ChatGPT (July 2026)

### Summary

Traditional inter-node MPI communication traverses network protocols and device software stacks even when nodes share a Compute Express Link memory pool. cMPI instead maps one-sided and two-sided point-to-point operations onto loads, stores, and copies in shared CXL memory. A shared-memory arena gives named-object allocation over the inflexible `devdax` interface and supports MPI remote-memory-access windows. Per-process single-producer/single-consumer queues coordinate messages without cross-node atomic operations, while cache flushes, fences, and non-temporal stores provide software coherence where hardware coherence is absent. Measurements on a real pooled-memory platform show raw CXL access with flushing has 7.2--8.1 times lower latency than TCP-based links. For small MPI messages, cMPI reaches up to 49 times lower latency and 72 times higher bandwidth than evaluated Ethernet and SmartNIC paths. Conjugate-gradient and miniAMR tests show that low latency benefits small-scale communication, whereas conventional high-bandwidth networking regains advantage as message sizes and node counts grow. The study establishes a working MPI design for CXL sharing, but the physical platform contains only two nodes, and cache maintenance plus CPU-driven copies limit large-message bandwidth and demonstrated scalability.

### Contributions

1. Implemented MPI one-sided and two-sided inter-node communication over a real CXL pooled-memory platform.
2. Designed a named-object shared-memory arena that makes `devdax` storage usable for MPI buffers and windows.
3. Replaced unsupported cross-node atomics with per-process single-producer/single-consumer message queues.
4. Provided software cache coherence using targeted flushes, fences, and non-temporal memory operations.
5. Quantified latency and bandwidth gains with microbenchmarks and application kernels while identifying large-message and scaling limits.
