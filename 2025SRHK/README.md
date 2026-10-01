# 2025SRHK

## ChatGPT (July 2026)

### Summary

Directional semi-Lagrangian splitting makes high-dimensional Vlasov solvers practical, but splitting the magnetic $\mathbf{v}\times\mathbf{B}$ rotation introduces interpolation error and numerical heating. For a constant background magnetic field, this paper transforms the full Vlasov equation to a rotating velocity grid that treats cyclotron rotation exactly and directionally splits only the remaining advections. The authors prove stability and second-order convergence of the rotating-grid Strang scheme under regularity, bounded-density, and consistency assumptions; the one-step flow error is $O(h^3)$. Numerical tests recover the expected second- and fourth-order rates for Strang and composed splittings. In stable and unstable neutralized ion Bernstein-wave problems, the rotating grid resolves more dispersion branches and accurate growth rates over a wider wavenumber range than fixed-grid splittings, while better preserving mass, the $L^2$ norm, and total energy. High-wavenumber accuracy remains limited by interpolation damping, and the analysis assumes a constant magnetic background.

### Contributions

1. Transformed the magnetized Vlasov equation onto a grid rotating with the cyclotron motion.
2. Reduced the number of directional interpolation steps while treating magnetic rotation exactly.
3. Proved stability, local third-order consistency, and global second-order convergence for rotating-grid Strang splitting.
4. Verified the predicted orders numerically, including a fourth-order composed method.
5. Improved ion Bernstein-wave dispersion and growth-rate calculations relative to fixed-grid splittings.
