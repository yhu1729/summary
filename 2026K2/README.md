# 2026K2

## ChatGPT (July 2026)

### Summary

This paper evaluates branch-free algorithms for fixed multiple-precision arithmetic represented by two, three, or four hardware floating-point components: double-double, triple-double, and quadruple-double precision. Error-free transformations and branch-free renormalization expose instruction-level parallelism to AVX2 on AMD EPYC and Neon on Qualcomm Snapdragon processors. Implementations are tested in real and complex Strassen matrix multiplication, real-coefficient polynomial evaluation at real and complex arguments, and a Durand--Kerner solver for a Chebyshev integration polynomial. The benchmarks preserve the intended significant-digit ranges while showing that branch elimination is precision- and architecture-dependent. It slows or does not improve double-double arithmetic, but typically accelerates triple- and quadruple-double work; real matrix multiplication gains average factors of about $1.2$--$1.5$ and $1.4$--$2.0$, respectively. Combining branch-free arithmetic with SIMD gives roughly $1.47$--$1.61$ speedups in the EPYC Chebyshev test. A three-real-multiplication complex formulation also becomes increasingly advantageous at higher precision and larger sizes.

### Contributions

1. Integrated branch-free triple- and quadruple-component arithmetic with AVX2 and Arm Neon vectorization.
2. Benchmarked real and complex matrix multiplication across x86 and Arm platforms with controlled numerical accuracy.
3. Quantified that branch-free conversion helps triple- and quadruple-double arithmetic but not double-double arithmetic.
4. Evaluated SIMD branch-free arithmetic in polynomial evaluation and a Durand--Kerner root solver.
5. Showed that three-real-multiplication complex arithmetic improves relative efficiency as precision and problem size grow.
