# 2025Z

## ChatGPT (July 2026)

### Summary

This paper analyzes distributed-memory algorithms for estimating the variance of a sample mean by bootstrap resampling. It compares two naive MPI baselines with two proposed strategies under explicit dataset size, resample count, process count, bandwidth, and per-process memory models. Data Broadcast and Statistic Aggregation computes local sample means and transmits only their first and second moments; this removes the resample count from the dominant communication term, reducing it from $O(DN)$ to $O(D)$ for dataset size $D$ and $N$ resamples. When no process can store all data, Distributed Data and RNG Synchronization partitions the dataset and gives every process the same pseudorandom index stream. Each process contributes partial sums for indices in its partition, using $O(D/P)$ memory across $P$ processes at an $O(NP)$ communication cost. The analysis therefore exposes a direct trade-off: aggregation minimizes communication when replicated data fit in memory, while synchronized generation bounds memory when they do not. Python/mpi4py sketches illustrate both designs. The work is theoretical rather than an empirical scaling study; latency, nonblocking communication, load imbalance, and heterogeneous systems remain open.

### Contributions

1. Formulated explicit communication, computation, and memory models for four MPI bootstrap strategies.
2. Replaced full-sample returns with sufficient-statistic aggregation for variance estimation.
3. Reduced the aggregation strategy's dominant communication complexity from $O(DN)$ to $O(D)$.
4. Designed synchronized pseudorandom resampling for datasets partitioned across process memories.
5. Characterized the $O(D)$-communication versus $O(D/P)$-memory trade-off between the proposed methods.
