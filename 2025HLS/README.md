# 2025HLS

## ChatGPT (July 2026)

### Summary

Hauck, Laiu, and Schnake combine high-order/low-order acceleration with a micro-macro decomposition for fully implicit time stepping of the BGK kinetic equation. The micro-macro representation splits the distribution into a local Maxwellian and a perturbation, allowing the nonequilibrium component to be compressed when the flow is close to equilibrium. Both HOLO and micro-macro HOLO are implemented with discontinuous Galerkin discretizations in phase space so that the kinetic and moment systems remain consistent. A linearized BGK analysis compares source iteration, HOLO, and micro-macro variants, while numerical tests on Sod shock tube and sudden wall heating problems assess accuracy, convergence, and compression. The results show that micro-macro HOLO preserves the acceleration properties of HOLO and can reduce storage near equilibrium, though compression gains are limited when boundary layers dominate nonequilibrium behavior. Future work targets stronger fluid solvers, hybrid iteration strategies, higher-dimensional problems, and more accurate collision models.

### Contributions

1. Combined micro-macro decomposition with HOLO acceleration for fully implicit BGK time stepping.
2. Implemented the coupled kinetic-moment methods with phase-space discontinuous Galerkin discretizations.
3. Analyzed convergence behavior of source iteration, HOLO, and micro-macro HOLO on linear BGK models.
4. Compared accuracy and performance on shock-tube and wall-heating benchmark problems.
5. Quantified when micro-macro compression helps and when boundary-layer nonequilibrium limits storage savings.
