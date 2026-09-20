# 2025S2

## ChatGPT (July 2026)

### Summary

This technical monograph documents the mathematics and implementation of VMEC++, a C++ reimplementation of the widely used VMEC fixed- and free-boundary ideal-MHD equilibrium solver with a Python-facing interface. It derives the toroidal-coordinate and Fourier representations, spectral condensation, radial discretization, force residuals, accelerated-descent iteration, radial preconditioning, and equilibrium outputs used to compute nested-flux-surface stellarator and tokamak equilibria. A major portion reconstructs NESTOR's free-boundary vacuum-field calculation, including singularity subtraction and analytical Fourier coefficients. Later chapters specify inputs and HDF5 outputs and derive post-processing quantities such as Mercier stability, rotational transform, current density, field-line following, inverse coordinate transforms, $\nabla\alpha$, and BNORM data. A Solov'ev tokamak equilibrium supplies analytical cross-checks. The work makes previously scattered legacy numerics reproducible while recording current VMEC++ limitations, notably incomplete support for non-stellarator-symmetric configurations.

### Contributions

1. Consolidated the toroidal-coordinate, Fourier-parity, quadrature, and spectral-condensation conventions needed to reproduce VMEC++ behavior.
2. Derived the fixed-boundary VMEC core, including magnetic representation, radial discretization, MHD forces, accelerated descent, and radial preconditioning.
3. Reconstructed the free-boundary NESTOR formulation from Green's identity through singularity cancellation and its numerical linear system.
4. Documented the software-facing numerical contract, including input parameters, unified HDF5 output, and compatibility mappings to legacy VMEC products.
5. Derived downstream quantities and verification paths, including Mercier stability, rotational transform, current density, field-line coordinates, inverse transforms, $\nabla\alpha$, BNORM, and a Solov'ev equilibrium.
