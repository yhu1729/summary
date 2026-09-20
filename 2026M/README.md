# 2026M

## Codex/ChatGPT (September 2026)

### Summary

This paper accelerates Steinhaus--Johnson--Trotter permutation generation through combinatorial partitioning and AVX2 byte shuffles. Two independent permutation streams occupy the $128$-bit halves of a $256$-bit register, with each lane generating one quarter of the factorial search space. A reflection property supplies the remaining half: permutations in the first half have element $0$ before element $1$, and reversing them covers the complementary half. Vectorized staircase insertion uses precomputed shuffle masks, while the lane width limits permutations to $n\leq16$ and parallel scheduling changes their output order. The paper also describes an optimized scalar version of Knuth's Algorithm P and separate vector kernels for benchmarking and callback-based use. On an Intel Core i7-8850H with GCC 15.2.0, the author reports approximately threefold normalized generation throughput over the optimized scalar baseline. The timed vector kernel excludes callback overhead and directly generates only half the permutations; these results therefore do not establish end-to-end application speedup or performance on other processors. Reported validation reaches $n=11$, with a benchmark at $n=13$.

### Contributions

1. Partitions the first half of the permutation space into two streams that can advance concurrently within one AVX2 register.
2. Uses the relative order of elements $0$ and $1$ to justify recovering the complementary half-space by reversal.
3. Combines staircase insertion with lane-local byte-shuffle masks for vectorized permutation generation up to $n=16$.
4. Provides distinct scalar, vector-benchmark, and callback-based C implementations, with checksum protection against dead-code elimination in the benchmark.
5. Reports hardware-specific normalized throughput gains over optimized Algorithm P while explicitly separating half-space kernel timing from callback processing.
