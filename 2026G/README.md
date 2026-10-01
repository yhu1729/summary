# 2026G

## ChatGPT (July 2026)

### Summary

This paper presents bsort, an in-place, non-comparison sorting algorithm for unsigned integers, two's-complement signed integers, and IEEE-754 floating-point values. It extends binary quicksort's bitwise partitioning with sign-aware direction changes. Floating-point values are ordered hierarchically by sign, exponent, and mantissa; negative partitions reverse the required directions. The paper specifies positions for infinities, signed zeros, and NaNs, placing NaNs at the array extremes according to sign and mantissa payload and ordering $-0$ before $+0$. Correctness is proved for the integer and floating-point procedures. For $n$ elements of word width $w$, bsort takes $O(wn)$ time and $O(w)$ recursion space, so fixed machine widths give linear scaling in $n$. C and C++ benchmarks show competitiveness with standard-library hybrid sorts for small element widths, but performance degrades relative to them as word width grows and depends on data distribution.

### Contributions

1. Unified in-place bitwise sorting for unsigned integers, signed integers, and floating-point values.
2. Derived sign-aware partition rules and a sign--exponent--mantissa hierarchy for IEEE-754 data.
3. Defined deterministic placement of infinities, signed zeros, and signed NaN payloads.
4. Proved $O(wn)$ running time and $O(w)$ auxiliary space for $w$-bit elements.
5. Benchmarked C and C++ implementations against optimized standard-library sorting routines across types and input distributions.
