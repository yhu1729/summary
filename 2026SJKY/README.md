# 2026SJKY

## ChatGPT (July 2026)

### Summary

This paper develops a multi-species nonlinear Rosenbluth-Fokker-Planck collision operator for discontinuous Galerkin kinetic plasma simulations. Distribution functions are represented with DG basis functions, while Rosenbluth potentials are computed with B-spline finite elements in a reduced two-dimensional velocity space aligned with a strong background magnetic field. To handle mass-disparate species, the potential is split into analytic and correction parts, and expensive Gaussian quadrature contributions are stored as precomputed integration matrices. Because standard upwinding is incompatible with those matrices, the method uses an HLL flux formulation for advective boundary terms. Mass conservation follows from the divergence structure, while added correction operators enforce momentum, energy, and stable collisional equilibrium. Benchmarks against hydrogen, electrons, tungsten, five-species relaxation, implicit large-time-step tests, and a circular-tokamak bootstrap-current case show good agreement with theory and near-ideal scaling with species count. The paper leaves adaptive velocity grids for strongly varying temperatures and flows as future work.

### Contributions

1. Formulated a DG-compatible nonlinear Rosenbluth-Fokker-Planck operator for multi-species kinetic plasma simulations.
2. Combined DG distribution functions with finite-element Rosenbluth potentials and precomputed quadrature matrices.
3. Introduced HLL fluxes compatible with matrix precomputation for advective terms.
4. Added correction operators for momentum, energy, and stable interspecies equilibrium under large mass ratios.
5. Validated accuracy, conservation, efficiency, implicit stepping, and bootstrap-current behavior through numerical benchmarks.
