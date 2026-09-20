# 2026BEAV

## ChatGPT (July 2026)

### Summary

PENCO is a physics-guided neural-operator framework for three-dimensional phase-field evolution. It can use either FNO-4D or a multi-head neural operator and augments data fitting with symmetric Gauss--Lobatto PDE residuals, consistency with a semi-implicit numerical teacher, low-frequency Fourier anchoring, free-energy dissipation, and epoch-dependent loss weights. Tests cover Allen--Cahn, Cahn--Hilliard, Swift--Hohenberg, phase-field-crystal, and molecular-beam-epitaxy equations on periodic cubes. Across in-distribution rollouts, the hybrid models reduce long-horizon drift and generally outperform purely data-driven operators; they also generalize to spherical, star-shaped, and toroidal initial conditions. The pure-physics model slightly outperforms PENCO for out-of-distribution Cahn--Hilliard evolution, where strict conservation dominates. Experiments use $32^3$ grids, two operator layers, and substantially shorter training than the original two-dimensional MHNO study. Current demonstrations are limited to periodic domains and phase-field systems; fracture, crack growth, nonperiodic boundaries, and realistic multiphysics geometries remain future work.

### Contributions

1. Unified physics, energy, and numerical-scheme consistency in a neural operator.
2. Added symmetric Gauss--Lobatto residual enforcement for stiff phase-field partial differential equations.
3. Enforced semi-implicit teacher consistency, spectral anchoring, and energy dissipation.
4. Evaluated five three-dimensional phase-field systems under fixed data budgets.
5. Demonstrated long-horizon and unseen-geometry improvements over FNO-4D and MHNO.
