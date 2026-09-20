# 2026PN

## ChatGPT (July 2026)

### Summary

This paper reconstructs a sparse or localized matrix $B$, especially a matrix function $f(A)$, using only black-box matrix-vector products. SpaMRAM treats each row as an unknown sparse signal and applies Gaussian sensing with normalized iterative hard thresholding, allowing recovery when the sparsity pattern is unknown and dominant entries are sufficiently distributed. BaMRAM targets banded matrices and functions with off-diagonal decay: deterministic probing vectors separate nearby diagonals, recover a prescribed band, and admit inexpensive Gaussian a posteriori error estimates. Entry-decay assumptions yield error bounds for both methods, although implicit decay constants make them chiefly explanatory rather than computable a priori. The construction extends to Kronecker sums through multidimensional probing patterns. Experiments on synthetic matrices, SuiteSparse problems, and graph communicability show accurate recovery of exponentials, square roots, logarithms, and localized network quantities. In scalability tests up to dimension 25,600, BaMRAM's required products are essentially dimension-independent for bounded bandwidth, while SpaMRAM grows slowly and sublinearly on the tested sparse family. Krylov approximation error eventually limits accuracy.

### Contributions

1. Introduced SpaMRAM for row-wise compressed-sensing recovery without a known sparsity pattern.
2. Introduced BaMRAM for deterministic recovery of banded matrices and off-diagonally decaying matrix functions.
3. Proved decay-based approximation bounds and supplied practical randomized error estimators.
4. Extended deterministic probing to matrices arising from Kronecker-sum structures.
5. Demonstrated recovery of matrix functions and network quantities with favorable scaling on synthetic and SuiteSparse examples.
