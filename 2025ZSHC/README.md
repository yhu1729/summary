# 2025ZSHC

## ChatGPT (July 2026)

### Summary

Grid-based Vlasov--Poisson solvers become prohibitively expensive in six-dimensional phase space. This paper extends the semi-Lagrangian adaptive-rank method from matrix representations to hierarchical Tucker tensors, enabling simulations through three spatial and three velocity dimensions. A compact quadratic reconstruction evaluates the distribution at characteristic feet with third-order space-time accuracy and $O(d^2)$ stencil complexity, while semi-Lagrangian tracing permits large time steps without dimensional splitting. A recursive hierarchical Tucker adaptive cross approximation samples selected tensor entries and adjusts ranks along a dimension tree. The self-consistent electric field is computed by an FFT-based low-rank Poisson solver that avoids rank-inflating Hadamard products. The resulting worst-case cost is $O(d^4Nr^{3+\lceil\log_2 d\rceil})$, linear in the per-dimension grid size $N$ for fixed dimension and rank. Landau-damping and two-stream tests in up to 3D3V recover expected electric-energy dynamics and fine phase-space structures while compressing storage. Rank growth tracks nonlinear complexity, but mass, momentum, and energy errors rise in late strongly nonlinear stages, motivating the authors' proposed extension of locally macroscopic conservation techniques.

### Contributions

1. Extended semi-Lagrangian adaptive-rank integration from matrices to general hierarchical Tucker tensors for up to 3D3V dynamics.
2. Developed a compact $O(d^2)$ reconstruction with third-order space-time accuracy and no dimensional splitting.
3. Introduced recursive hierarchical Tucker adaptive cross approximation using only selected tensor entries.
4. Constructed an FFT-based low-rank Poisson solver that avoids rank-inflating tensor products.
5. Demonstrated adaptive compression and resolved kinetic structures in high-dimensional Landau-damping and two-stream benchmarks.
