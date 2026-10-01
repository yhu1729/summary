# 2026HXHW

## ChatGPT (July 2026)

### Summary

Regular two-dimensional blocking wastes parallelism in sparse LU factorization when fill is concentrated near the diagonal and lower-right region. This paper introduces a diagonal-block feature that measures cumulative nonzero distribution locally and globally, then uses it to choose unequal block sizes. Dense regions receive fine blocks and sparse regions coarse blocks, balancing work both among blocks at one dependency-tree level and across levels. The method is integrated into a PanguLU-style numerical factorization and evaluated on NVIDIA A100 GPUs. Across the test matrices, it reaches geometric-mean speedups of $1.50\times$ over PanguLU and $3.32\times$ over SuperLU_DIST on one GPU, and $1.40\times$ and $3.84\times$, respectively, on four GPUs. Benefits are largest for strongly irregular fill patterns; nearly uniform diagonal distributions can show little gain. Irregular metadata and lookups increase preprocessing cost, which the authors accept because numerical factorization dominates total time.

### Contributions

1. Defined a diagonal-block feature that captures local sparse-fill distribution.
2. Designed an irregular blocking rule with fine dense blocks and coarse sparse blocks.
3. Balanced numerical work within and across dependency-tree levels.
4. Demonstrated geometric-mean speedups on one and four NVIDIA A100 GPUs.
5. Characterized when irregularity yields gains and when preprocessing overhead or uniform structure limits them.
