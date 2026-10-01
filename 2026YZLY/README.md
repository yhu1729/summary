# 2026YZLY

## Claude (September 2026)

### Summary

TokaGLINT is a GPU linear solver for the implicit electromagnetic field update in SymPIC, a symplectic, charge-conserving particle-in-cell code for tokamaks. Replacing the explicit field step with a Crank–Nicolson finite-difference time-domain discretization removes the electromagnetic Courant limit while keeping the symplectic structure, but requires solving a metric-weighted curl–curl system on a cylindrical mesh at every step. The solver uses pipelined BiCGStab, which hides global reductions behind local work, preconditioned by a hierarchical additive Schwarz method: overlapping subdomains across GPUs, each split into several overlapping subdomains on one GPU. Each small subdomain is solved exactly by singular-value-based discrete transforms of the difference operators, which decouple unknowns in two directions despite the radial metric and leave diagonal plus $(2n_x)\times(2n_x)$ block systems with precomputed inverses. Equal-radius subdomains share operators and are binned so transforms run as batched GEMMs and block solves fuse into GEMMs. The preconditioner keeps BiCGStab near 7–8 iterations in weak scaling and far below Jacobi, SOR, ISAI, ILUT, and algebraic multigrid counts at large time steps. Results include 2.67–3.03× speedups over unpreconditioned HYPRE BiCGStab, 90.1% weak-scaling efficiency from 16 to 10,000 GPUs, 53.9% strong-scaling efficiency from 672 to 10,752 GPUs, and energy held within ±0.1% over $10^6$ steps.

### Contributions

1. Recast SymPIC's electromagnetic update as a field-implicit Crank–Nicolson scheme on cylindrical meshes, expressed as a metric-weighted curl–curl system for the discrete 1-form unknowns.
2. Extended discrete-transform fast exact solvers from Cartesian to cylindrical curl–curl operators, reducing each subdomain solve to diagonal and radial-line block systems with $O(N^{4/3})$ storage.
3. Designed a two-level additive Schwarz preconditioner that places several overlapping subdomains on each GPU, exchanging overlaps through high-bandwidth memory, and paired it with communication-hiding BiCGStab.
4. Introduced geometry-driven binning of equal-radius subdomains with custom data layouts, turning transforms into batched GEMMs and fusing block-diagonal solves, with one MPI process managing all subdomains on a GPU.
5. Integrated the solver into SymPIC and validated it with toroidal wave-propagation and long-time magnetized-plasma energy-conservation tests.
