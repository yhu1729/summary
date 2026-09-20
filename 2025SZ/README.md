# 2025SZ

## ChatGPT (July 2026)

### Summary

This paper studies prefix sums through matrix identities, decomposing triangular all-ones matrices into sums of Kronecker products. The decomposition exposes a recursive structure behind known prefix circuits and shows where Brent-Kung-style constructions waste one output per recursive call. Removing that deficiency leads to a parameterized family of zero-deficiency prefix circuits with constant fan-out per level. For block size $s$, the circuits have depth bounded by $s\lceil\log_s n\rceil+O(1)$; choosing $s=3$ gives about $1.893\log n+O(1)$ depth, below the $2\log n$ depth of classic zero-deficiency families. The construction is LOGTIME-uniform and retains linear size. The authors then use the prefix circuits for quantum carry-lookahead addition, obtaining quantum adders with $O(n)$ Toffoli gates, $O(n)$ auxiliary qubits, and $1.893\log n+O(1)$ Toffoli depth. The work connects linear-algebraic identities, parallel prefix circuits, and quantum arithmetic design.

### Contributions

1. Derived a Kronecker-product decomposition of triangular prefix-sum matrices.
2. Identified and removed the recursive deficiency in Brent-Kung-style prefix circuits.
3. Constructed LOGTIME-uniform zero-deficiency circuits with constant fan-out per level.
4. Optimized block size to obtain sub-$2\log n$ prefix depth with linear size.
5. Applied the circuits to quantum adders with improved Toffoli depth and linear resource counts.
