# 2026LMHL

## ChatGPT (July 2026)

### Summary

TRIMEG-GKX is presented as an electromagnetic gyrokinetic particle-in-cell code for tokamak core plasma simulations. The code combines object-oriented multi-species modeling, a mixed-variable/pullback electromagnetic formulation, and a high-order piecewise field-aligned finite element method using cubic B-splines. Its field-aligned discretization reduces grid requirements along magnetic-field directions, while particle decomposition with domain cloning replaces traditional domain decomposition for the demonstrated use cases. The paper emphasizes filter- and buffer-free treatment of the strong gyrocenter equations, plus cache optimization for particle-field interpolation that yields a reported tenfold speed-up in typical single-harmonic simulations. Benchmarks cover energetic-particle-driven Alfvén eigenmodes, reversed-shear Alfvén eigenmodes, ion-temperature-gradient modes, and kinetic ballooning modes in ad hoc and experimentally reconstructed ASDEX Upgrade, TCV, and JET equilibria. The work establishes the code's numerical scope and benchmark behavior; nonlinear physics validation, open-field-line configurations, and collisions are left as future development paths.

### Contributions

1. Described TRIMEG-GKX as an electromagnetic, multi-species gyrokinetic particle code for core tokamak instabilities.
2. Integrated a high-order piecewise field-aligned finite element discretization into the particle-in-cell workflow.
3. Implemented mixed-variable/pullback electromagnetic dynamics without relying on Fourier filters or numerical buffers.
4. Reported cache and parallelization choices that improve particle-field interpolation and multi-harmonic simulations.
5. Benchmarked Alfvénic, ion-temperature-gradient, and kinetic-ballooning cases in idealized and reconstructed equilibria.
