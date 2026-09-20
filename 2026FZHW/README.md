# 2026FZHW

## ChatGPT (July 2026)

### Summary

This work extends the cell-based ECOGEN adaptive-mesh framework into an open-source C++ solver for multiscale supersonic reacting flows. It solves the compressible, multicomponent reactive Navier--Stokes equations using thermally perfect species, mixture-averaged transport, and detailed finite-rate chemistry supplied through Cantera. A MUSCL finite-volume discretization reconstructs interface states; a multicomponent HLLC Riemann solver with low-Mach correction improves inviscid-flux accuracy for detonations, while a skewness-corrected central scheme handles viscous fluxes. Hydrodynamics advances with second-order Runge--Kutta integration, and operator-split chemical source terms use Cantera solvers of up to sixth order. To concentrate resolution on physically important structures, the authors design a three-stage AMR strategy that separately addresses inert-flow features, flame fronts, and coupled shock--flame regions, including secondary shocks missed by simple gradient criteria. They also derive a theoretical AMR-to-uniform-grid speedup ratio from advancement costs and show agreement with measured speedups. Validation spans one-, two-, and three-dimensional convection, diffusion, planar flames, inert and reacting shock--bubble interactions, planar detonations, and cellular detonation structures. The result is a validated GPLv3 tool for studying shock-induced ignition, Richtmyer--Meshkov dynamics, supersonic mixing, and combustion across widely separated length scales.

### Contributions

1. Extends ECOGEN into a GPLv3 solver for compressible multicomponent reacting flows with detailed thermochemistry and transport through Cantera.
2. Introduces a multicomponent HLLC solver with low-Mach correction that improves detonation simulations over the conventional HLLC formulation.
3. Develops a three-stage AMR strategy specialized for inert-flow structures, flame fronts, and coupled shock--flame interactions.
4. Derives an AMR speedup model from advancement costs and validates its theoretical predictions against measured speedups.
5. Validates accuracy and efficiency across inert and reacting one-, two-, and three-dimensional benchmarks, including shock--bubble interactions and cellular detonations.
