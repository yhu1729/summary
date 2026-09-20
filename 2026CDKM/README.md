# 2026CDKM

## ChatGPT (July 2026)

### Summary

Catalytic computation gives an algorithm a large read--write memory initially filled with arbitrary data, provided that the memory is restored exactly afterward. The paper asks whether such full memory can reproduce leading polynomial-time, sublinear-space algorithms while retaining only logarithmic clean workspace. It answers affirmatively for directed $s$--$t$ connectivity, edit distance, longest common subsequence, and discrete Fr\'echet distance. For connectivity, it combines a long/short-path decomposition with reversible flow propagation. Representative vertices are generated from pairwise-independent hashes sampled through an explicit expander walk, reducing the random seed to logarithmic length. For grid problems, the authors propagate weighted path sums, encode additive path costs multiplicatively, and reconstruct large integers from Chinese-remainder residues. These techniques produce polynomial-time algorithms with $O(\log n)$ ordinary workspace and sublinear catalytic space matching the established $n/2^{\Theta(\sqrt{\log n})}$ frontier. The work also supplies the first such sublinear-space result for discrete Fr\'echet distance under its stated metric assumptions.

### Contributions

1. Gave deterministic polynomial-time directed-connectivity algorithms with logarithmic clean workspace and frontier-level sublinear catalytic space.
2. Gave a one-sided-error randomized connectivity variant using only logarithmically many random bits.
3. Built representative graph subsets from pairwise-independent hashes and explicit expander walks without storing the subset in clean memory.
4. Developed catalytic weighted-reachability algorithms for directed grid graphs using reversible flow propagation and Chinese-remainder representations.
5. Applied the grid framework to exact edit distance, longest common subsequence, and discrete Fr\'echet distance.
