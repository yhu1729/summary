# 2026GGT

## ChatGPT (September 2026)

### Summary

PACO is a parallel fast Fourier transform that simultaneously targets cache-efficient local computation and minimal global data movement. It performs a local FFT, one global permutation, and a second local FFT. Recursive local stages partition transform and batch dimensions without knowing cache parameters. Rather than materializing each transpose-like layout induced by the recursion, PACO defers these layouts, composes them into a base-$b$ digit reversal, and fuses that permutation with the ownership redistribution already required between transform dimensions. Under an exact base-$b$ slab decomposition in a hybrid ideal-cache/Bulk Synchronous Parallel model, an $N$-point transform on $p$ processors has optimal maximum work $\Theta((N/p)\log N)$, optimal cache complexity $\Theta((N/(pB))(1+\log_M N))$, and exactly one global redistribution. Every source--destination pair transfers $N/p^2$ elements, and the output uses factor-swapped slab ownership. The analysis assumes bounded power-of-two radix, exact divisibility, homogeneous parameters, no replication, and one-dimensional slab distributions.

### Contributions

1. Designed a fully cache-oblivious distributed FFT with a single global redistribution round.
2. Represented recursive layout changes lazily and composed them into one digit-reversal permutation.
3. Fused local-layout permutation with the unavoidable global ownership change.
4. Proved optimal per-processor work and ideal-cache complexity under the stated decomposition model.
5. Established balanced pairwise communication and optimal migration volume for the prescribed ownership contract.
