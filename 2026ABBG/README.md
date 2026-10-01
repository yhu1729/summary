# 2026ABBG

## ChatGPT (July 2026)

### Summary

This work presents a C++ finite-element framework for large-scale computational fluid dynamics, discrete-particle simulation, and coupled multiphysics. Built on deal.II, it combines stabilized continuous Galerkin formulations with distributed-memory parallelism, dynamic mesh adaptation, load balancing, and high-order isoparametric elements. Three fluid linear-algebra paths--monolithic matrix-based, block matrix-based, and matrix-free--support problems ranging from flexible tetrahedral meshes to hexahedral simulations exceeding one billion unknowns. The physics modules cover incompressible Newtonian and generalized-Newtonian flow, heat transfer, tracer transport, Volume-of-Fluid and Cahn--Hilliard two-phase models, and discrete element methods. Particle coupling supports unresolved CFD--DEM for millions of spheres and resolved immersed-boundary CFD--DEM for fewer complex particles, while a Nitsche immersed-boundary formulation handles moving geometries. A common parameter-file workflow and modular solver architecture let users combine physics and extend models. Verification and application examples address turbulent Taylor--Couette flow, granular discharge, rising bubbles, fluidized beds, settling particles, and conjugate heat transfer, comparing against analytical, experimental, or reference solutions. Engineering maturity is supported by more than 450 automated tests and 74 documented examples with meshes and post-processing scripts. The framework therefore couples research-grade high-order numerics, scalable execution, multiphase breadth, and reproducible onboarding in one open-source platform.

### Contributions

1. Delivers an open-source, parallel high-order finite-element framework for chemical and manufacturing flow simulations on the deal.II infrastructure.
2. Unifies single-phase CFD, heat transfer, fluid-fluid models, DEM, and resolved and unresolved CFD--DEM within a modular multiphysics architecture.
3. Provides matrix-based, block matrix-based, and matrix-free solver paths, with the latter demonstrated on problems exceeding one billion unknowns.
4. Integrates dynamic mesh adaptation for hexahedral CFD meshes and extends parallel load balancing to DEM and coupled CFD--DEM workflows.
5. Establishes reproducibility and extensibility through more than 450 automated tests, 74 documented examples, and validations against analytical, experimental, and reference results.
