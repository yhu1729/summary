# 2026GNY

## ChatGPT (July 2026)

### Summary

Entries of inverses of diagonally dominant matrices encode quantities such as random-walk escape probabilities and hitting times, which may be exponentially small. Normwise error bounds therefore do not provide useful relative accuracy for every entry without high bit complexity. This paper studies multiplicative, entrywise $\exp(\varepsilon)$ approximation for row diagonally dominant $L$-matrices (RDDL) and symmetric diagonally dominant $M$-matrices (SDDM). For floating-point RDDL inputs, it gives a cubic-time inversion algorithm whose running time is condition-number independent and conditionally optimal under the all-pairs shortest-paths conjecture. For fixed-point inputs, a threshold-decay framework yields SDDM linear solves in $\widetilde O(m\sqrt n)$ bit operations and inversion in $\widetilde O(mn)$. For directed RDDL matrices, the authors obtain a linear solve in $\widetilde O(mn^{1+o(1)})$ and inversion algorithms with costs $\widetilde O(n^{\omega+1/2})$ or $\widetilde O(mn^{3/2+o(1)})$. The analysis combines Schur complements, random-walk interpretations, and graph shortcutters, and transfers the guarantees to all-pairs escape probabilities and hitting times. The results separate arithmetic-operation speed from the precision cost required for entrywise accuracy.

### Contributions

1. Formulated and analyzed multiplicative entrywise approximation for inverses and solutions of RDDL and SDDM systems.
2. Gave a condition-number-independent cubic-time algorithm for floating-point RDDL inversion.
3. Proved conditional optimality of the floating-point algorithm through a reduction from all-pairs shortest paths.
4. Developed fixed-point SDDM algorithms requiring $\widetilde O(m\sqrt n)$ bit operations for one solve and $\widetilde O(mn)$ for inversion.
5. Derived subcubic directed-RDDL algorithms and corresponding guarantees for escape probabilities and hitting times.
