# 2024T

## ChatGPT (July 2026)

### Summary

These lecture notes develop parallel computing from analytical foundations through practical programming on shared- and distributed-memory systems. They distinguish parallel computing from concurrent and distributed computing, introduce machine and programming models such as RAM, PRAM, shared memory, and message passing, and define the metrics needed to judge algorithms: time, work, cost, speedup, efficiency, load balance, and scalability. Classical limits, including Amdahl's law and memory-bandwidth constraints, are connected to empirical benchmarking. The notes then build reusable design patterns--task graphs, pipelines, stencils, work pools, domain decomposition, reductions, scans, and collective communication--and analyze algorithms for merging, prefix sums, searching, sorting, and linear algebra. Shared-memory programming is treated through C, POSIX threads, and OpenMP, including synchronization, races, memory consistency, scheduling, and NUMA effects. Distributed-memory programming receives detailed MPI coverage: communicators, datatypes, point-to-point, nonblocking, persistent and one-sided communication, collectives, topology, and performance models. Correct C-like examples and extensive exercises turn the theory into implementation and benchmarking practice. GPUs and randomized algorithms are deliberately excluded, but the principles of locality, bandwidth, overhead, and scalable work remain applicable across parallel architectures.

### Contributions

1. Unifies theoretical algorithm analysis with practical shared- and distributed-memory programming in a course-length reference.
2. Develops a consistent framework for reasoning about parallel time, work, cost, speedup, efficiency, load balance, and scalability.
3. Organizes reusable parallel patterns and analyzes representative algorithms for merging, prefix sums, searching, sorting, and linear algebra.
4. Provides detailed, concept-driven coverage of POSIX threads, OpenMP, and MPI, including synchronization, advanced communication modes, and performance implications.
5. Supplies correct C-style examples and extensive exercises designed for implementation projects, benchmarking, self-study, and classroom assessment.
