# 2025JM

## Codex/ChatGPT (September 2026)

### Summary

A closed string is a single character or has a nonempty border—a matching proper prefix and suffix—with no internal occurrence. This paper represents all closed substring occurrences of a length-$n$ string using $O(n\log n)$ intervals of admissible lengths, avoiding explicit enumeration of a potentially quadratic output. A maximal right-closed array records substrings that cease to be closed when extended one position to the right, together with their border lengths. Two algorithms construct this array in $O(n\log n)$ time with $O(n)$ auxiliary space: one merges ordered suffix-position sets while scanning suffix and longest-common-prefix arrays; the other modifies Crochemore's equivalence-class refinement. The stored output may itself require $O(n\log n)$ space. A further scan extracts substrings maximal under both left and right extension. An exact parity-dependent count of maximal closed substring occurrences in Fibonacci words approaches $1.382$ times the word length. Experiments favor equivalence-class refinement for Fibonacci and Tribonacci words, and the suffix-array implementation for the other tested sequences. These timings compare the two proposed implementations; no experimental comparison with the earlier suffix-tree algorithm is reported.

### Contributions

1. Introduced an interval representation grouping closed occurrences by starting position and consecutive allowable lengths, with an $O(n\log n)$ storage bound.
2. Constructed the maximal right-closed array using longest-common-prefix transitions and ordered-set union operations, proving $O(n\log n)$ time and linear auxiliary space.
3. Adapted Crochemore's refinement algorithm to obtain the same array directly from the string, using level timestamps to avoid quadratic auxiliary storage.
4. Derived the exact Fibonacci-word count $M(f_k)=F_k+F_{k-2}-1$ for odd $k$ and $F_k+F_{k-2}-2$ for even $k$, for $k\geq5$ and $F_k=|f_k|$, by classifying singleton occurrences, runs, and maximal gapped repeats.
5. Supplied implementations and experiments separating the algorithms' behavior on repetitive words, Thue–Morse words, digits of $\pi$, biological sequences, and random strings.
