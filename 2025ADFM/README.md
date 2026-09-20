# 2025ADFM

## ChatGPT (July 2026)

### Summary

The paper analyzes an Ozaki-style scheme that emulates binary64 matrix
multiplication with fast integer matrix-multiply--accumulate units. Rows of one
factor and columns of the other are scaled, decomposed into short integer
slices, multiplied exactly, and accumulated in floating-point arithmetic. New
forward-error bounds expose separate row- and column-scaling factors and permit
different slice counts for the two operands. Because those factors are
available during slicing, the authors propose a cheap search for the smallest
pair of slice counts meeting a target bound. Experiments confirm that asymmetric
slicing can retain accuracy with fewer products, but badly scaled operands may
require impractically many slices. On random matrices, a prototype NVIDIA
integer implementation reaches binary64-like accuracy with seven slices; some
higher-level MAGMA factorizations require eight. Performance gains at acceptable
accuracy appear on a Blackwell B200, whose INT8-to-binary64 throughput ratio is
large, but not on the tested Grace-Hopper system. The scheme is therefore not a
general binary64 replacement, especially for extreme scaling or IEEE special
values.

### Contributions

1. Derived error bounds for integer-sliced floating-point matrix multiplication.
2. Quantified the separate effects of badly scaled rows and columns on accuracy.
3. Proposed an inexpensive input-dependent search for asymmetric slice counts.
4. Tested accuracy inside block LU, QR, eigensolver, and singular-value algorithms.
5. Measured the accuracy--performance tradeoff on NVIDIA Grace-Hopper and Blackwell GPUs.
