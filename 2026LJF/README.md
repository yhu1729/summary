# 2026LJF

## Claude (September 2026)

### Summary

The authors present cuGMEC, a gyrokinetic–magnetohydrodynamic (MHD) hybrid code written from scratch in CUDA C++ for GPUs to simulate Alfvén eigenmodes driven by energetic particles (EPs) in tokamaks. Relative to the earlier CPU code GMEC, the fluid model adds thermal-ion finite-Larmor-radius (FLR) effects to the gyrokinetic vorticity equation through a Padé approximant, a parallel electric field in the generalized Ohm's law, an electron continuity equation with an isothermal closure, and all nonlinear terms; thermal ions and EPs are advanced by gyrokinetic $\delta f$ particle-in-cell (PIC) and enter through their perturbed pressures. Five-point central differences and fourth-order Runge–Kutta are applied in Boozer, field-aligned, and shifted-metric coordinates built from DESC equilibria. Multi-GPU runs partition the poloidal direction, exchange ghost cells through NCCL and MPI, all-reduce particle pressures, and solve the gyrokinetic Poisson equation with cuDSS. Benchmarks against theory and other codes cover tearing modes, toroidal and reversed-shear Alfvén eigenmodes, FLR radiative damping, nonlinear multi-$n$ coupling, and cyclone-base-case ion-temperature-gradient and kinetic ballooning modes; trapped-electron modes are outside the model because electrons are fluid. On A800 GPUs, strong scaling to 32 GPUs retains 81.7% (MHD) and 72.0% (full model) efficiency, and one GPU replaces about 21.9 Xeon Gold 6348 CPUs.

### Contributions

1. Diagnosed an odd–even decoupling instability along field lines caused by central differencing of $\boldsymbol{b}_0\cdot\nabla$ on a collocated grid and removed it by staggering only the $y$ grid, on which $\delta A_\parallel$ and $\delta J_\parallel$ are evolved.
2. Replaced fully expanded stencils (25 coefficients for $\delta J_\parallel$) with Mathematica-generated compressed coefficients multiplying retained derivatives (6 coefficients), gaining about 1.5–1.75× in double precision, and fixed $N_z$ to a half or full warp so that interpolation along $z$ can use warp-shuffle instructions.
3. Accelerated PIC field gathering by storing the eight gathered fields contiguously per grid point (3.0–4.25× on A800, 2.0–3.5× on RTX 4090) and by radix-sorting particles by cell every 20 steps to improve cache reuse.
4. Verified the FLR radiative damping scaling, with fitted slope and intercept within 4.8% and 8.5% of theory, and nonlinear mode generation in which the $n=0,12,18$ growth rates are 1.95, 1.93, and 2.98 times that of $n=6$.
5. Provided per-step timing tables versus particles per cell and gyro-average points for single- and multi-mode grids, and a GPU-to-CPU cost equivalence of 17.4× for MHD and 22.5× for PIC.

### Comments

- Section 3.2, Fig. 3: the text states that "the shuffle instruction provides further improvement of about 1.5–2.0x on top of coefficient compression", but in the double-precision panels of Fig. 3 compression plus shuffle exceeds compression alone by only about 1.04–1.09× (RTX 4090, L40) and 1.24–1.40× (V100, A800); the stated range matches only the single-precision panels.
- Section 3.4, Fig. 4: the text states "Speedups of 2.0x-3.0x and 5.0x-8.0x are achieved on the A800 and RTX 4090", but the RTX 4090 double-precision sorting curves lie at about 1.0–1.9×, and the claim that the two optimizations together "achieve a speedup of approximately 10.0x-25.0x for the PIC component" exceeds the products of the rearrangement and sorting speedups in Fig. 4 at matching precision and gyro-average points, which stay below about 16×; unresolved.
- Section 4.4, text after Eq. (26): "The background ions are hydrogen with $\rho_i/a = 125$" conflicts with the stated $T_\mathrm{ref}=2.2$ keV, $B_0=2$ T, and $a=0.36R_0$ with $R_0=0.835$ m, which give a gyroradius of a few millimetres and $a/\rho_i\approx125$; the evident intended reading is $a/\rho_i=125$, the ratio used in Section 4.2.
