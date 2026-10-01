# 2026FW

## Claude (September 2026)

### Summary

High-order WENO and Hermite WENO (HWENO) shock-capturing schemes spend much of their cost on wide stencils, stagewise nonlinear weights, and characteristic decompositions. The authors propose finite-average-moment (FAM) schemes that evolve only the $P^1$ moment state, cell averages and scaled first moments, with a DG-style weak form and SSP-RK3, and obtain orders $k=3,4,5,6$ from fixed linear, polynomially exact reconstructions on compact stencils: three cells in one dimension and a $3\times3$ patch on uniform Cartesian grids in two. Nonlinear stabilization is a single oscillation-elimination (OE) step after the final Runge–Kutta stage, an exact exponential damping of the first moments driven by interface jumps of the reconstruction, which preserves cell averages and changes smooth solutions only by $\mathcal O(\Delta x^{k+1})$. For linear advection without OE, Fourier analysis gives a $k$th-order physical mode, a strongly damped spurious mode, and $(k+1)$th-order cell-average superconvergence. Smooth Burgers and Euler tests confirm these orders, and Buckley–Leverett and one- and two-dimensional Euler shock problems, reconstructed componentwise in conservative variables, show no visible oscillations; strong-shock tests need a positivity-preserving limiter. FAM5 and FAM6 run faster than MR-WENO5, HWENO-U, and OE-HWENO, with time ratios down to 0.10, whereas FAM3 is slower than MR-WENO3. No nonlinear stability theory is given.

### Contributions

1. Decoupled formal order from the number of evolved unknowns: two per component per cell in one dimension and three in two, with order supplied by paired auxiliary polynomials, including incomplete quartic and sixth-degree ones in two dimensions.
2. Proved unique solvability and polynomial exactness of the compact reconstruction systems, and cell-average preservation, nonexpansive damping, and accuracy preservation of the one- and two-dimensional OE steps.
3. Derived sampled admissible CFL numbers 0.40, 0.44, 0.58, and 0.56 for $k=3,4,5,6$ from the SSP-RK3 amplification matrix of the linear backbone.
4. Introduced a Type II damping coefficient normalized by an unnormalized local sum, which reduces undershoots and preserves small structures relative to the globally normalized Type I in a multiscale Lax problem.
5. Attributed 77–85% of HWENO-U and OE-HWENO runtimes to stagewise reconstruction and showed that local characteristic variables increased FAM5 runtime by factors of 1.25 and 1.80 without visible change in the displayed densities.

### Comments

- Abstract: "the FAM schemes deliver significantly lower complete-run wall-clock times compared to" MR-WENO, HWENO-U, and OE-HWENO, but Table 8 gives FAM3 versus MR-WENO3 time ratios of 1.42 (Sedov) and 1.61 (LeBlanc), a matched-order pair that §4 lists among the emphasized comparisons; the claim holds only for the FAM5 and FAM6 comparisons.
- Fig. 2: the caption describes the "$L^1$ error of the density cell averages versus wall-clock time for the 1D smooth Euler test", but the plotted error ranges match the Burgers errors of Table 5, not the Euler errors of Table 6; MR-WENO3 runs from about $10^{-3}$ to $10^{-5.3}$, as in Table 5 ($9.10\times10^{-4}$ to $4.85\times10^{-6}$) rather than Table 6 ($4.63\times10^{-3}$ to $1.12\times10^{-4}$), and FAM6 starts near $10^{-5.8}$ (Table 5: $1.64\times10^{-6}$; Table 6: $9.84\times10^{-9}$), so the error axes repeat Fig. 1; the intended Euler data are unresolved.
- Table 14, $k=6$: Appendix L defines the FAM6 reconstruction as $\sum_{\ell=0}^{20}c_\ell\phi^{(\ell)}_{i,j}$, discarding $c_{21}$ and $c_{22}$ of the auxiliary polynomial $Q_6$, and (2.12) takes jumps of the reconstruction, but the printed $\mathbf A_6$, $\mathbf B_6$, and $\mathbf C_6$ equal the face-center jumps of the unprojected $Q_6$ computed from the printed coefficients $c_0,\dots,c_{22}$, whereas the rows $k=3,4,5$ correspond to the projected polynomials; which jumps the computations use is unresolved.
