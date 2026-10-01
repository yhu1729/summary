# 2026BFKP

## ChatGPT (July 2026)

### Summary

High-order finite elements on triangles and tetrahedra can make local Riesz-map solves scale prohibitively with polynomial degree $p$. This paper constructs alternative bases for the same simplicial de Rham spaces using integral moments against numerically generated polynomials orthogonal in two inner products. The resulting cell matrices have weak interior--interface and interior--interior couplings. Neglecting selected couplings yields sparse auxiliary operators, and combining the split with Pavarino, Arnold--Falk--Winther, and Hiptmair patch decompositions produces $p$-robust preconditioners in the targeted stiffness-dominated regime. In three dimensions, setup falls from the naive $O(p^9)$ cost to $O(p^6)$, with $O(p^4)$ storage and lower application cost. Incomplete Cholesky factorizations preserve the static-condensation sparsity pattern. Numerical tests across $H(\mathrm{grad})$, $H(\mathrm{curl})$, and $H(\mathrm{div})$ confirm bounded iteration counts in the predicted regimes. Augmented-Lagrangian block preconditioners then extend the solvers to Hodge Laplacians. Robustness for strongly mass-dominated parameter choices is not generally guaranteed.

### Contributions

1. Constructed high-order simplicial de Rham bases with provably weak interior coupling.
2. Derived interior--interface splittings compatible with standard patch-space decompositions.
3. Reduced three-dimensional setup complexity from $O(p^9)$ to $O(p^6)$.
4. Built sparse incomplete-Cholesky patch solvers with favorable degree scaling.
5. Applied the Riesz-map solvers to augmented-Lagrangian preconditioning of Hodge Laplacians.
