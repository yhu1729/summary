# 2026DGNP

## Codex/ChatGPT (September 2026)

### Summary

This paper extends hierarchical sparse-grid particle-in-cell methods for the Vlasov–Poisson system to resolve localized plasma structures while retaining reduced particle noise. An energy-based B-spline approximation space prioritizes accuracy in the $H^1$ seminorm, which measures electric-field error through the potential gradient. Generalized sparse-grid spaces enrich the hierarchy toward full-grid resolution. Local adaptation selects basis functions using normalized density coefficients, called hierarchical surpluses. An incremental algorithm evaluates candidate subspaces with Schur complements and reused Cholesky factorizations, avoiding a solve over the complete enriched space. Two-dimensional manufactured-solution and diocotron-instability tests distinguish spatial bias from statistical error and demonstrate improved density reconstruction with fewer active nodes. In one manufactured-solution benchmark, the adaptive method uses approximately $17$ times fewer particles and $45$ times fewer nodes than standard PIC, with roughly fivefold shorter execution time. The results support local refinement as a way to balance sparse-grid noise reduction against representation error; three-dimensional validation remains future work.

### Contributions

1. Introduces an energy-based hierarchical approximation space with $O(h^{-1})$ degrees of freedom, targeting $H^1$ accuracy without the conventional sparse-grid dimension factor $|\log h|^{d-1}$.
2. Defines generalized sparse-grid spaces that add hierarchical levels, supplying additional basis functions for structures poorly resolved by conventional sparse grids.
3. Develops a local adaptation criterion based on normalized density surpluses, retaining significant basis functions and removing insignificant degrees of freedom.
4. Derives an incremental refinement algorithm using Schur-complement reduction and reusable Cholesky factors to assess candidate subspaces without solving the complete generalized mass system.
5. Demonstrates restored second-order spatial convergence for a challenging diocotron initial density and substantial particle, node, and runtime reductions in separate two-dimensional accuracy benchmarks.
