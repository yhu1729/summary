# 2024K

## ChatGPT (July 2026)

### Summary

The paper studies accuracy-aware floating-point compression for standard $\mathcal H$-, uniform $\mathcal H$-, and $\mathcal H^2$-matrix representations and its effect on bandwidth-bound matrix--vector multiplication. Variable-accuracy low-rank compression assigns precision according to singular-value contributions while keeping the total perturbation near the requested tolerance. Compression is fused into multiplication so coefficients are decompressed only when consumed. Experiments show the largest memory savings for $\mathcal H$-matrices, followed by uniform $\mathcal H$- and $\mathcal H^2$-matrices; adaptive floating-point compression outperforms a fixed-exponent alternative. Reduced bandwidth demand yields roughly $2$--$3\times$ speedup for $\mathcal H$-matrix multiplication and $1.5$--$2.5\times$ for uniform $\mathcal H$-matrices, with smaller gains for $\mathcal H^2$. Benefits grow with problem size but decline at tighter accuracy.

### Contributions

1. Extended floating-point compression analysis across three major hierarchical-matrix formats.
2. Adapted variable-accuracy low-rank compression to shared and nested cluster bases with controlled error.
3. Designed fused matrix--vector kernels that decompress coefficients only on access.
4. Quantified format-dependent storage savings and explained them through low-rank and cluster-basis structure.
5. Demonstrated bandwidth-driven speedups and evaluated their distance from roofline limits.
