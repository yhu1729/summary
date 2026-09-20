# 2025CLLZ

## ChatGPT (July 2026)

### Summary

The authors propose a high-order energy-conserving semi-Lagrangian discontinuous Galerkin (ECSLDG) method for the Vlasov--Ampère system. The Vlasov equation is reduced by operator splitting to one-dimensional advection problems solved with SLDG, providing high-order spatial accuracy, local mass conservation, and freedom from a CFL stability restriction. A semi-implicit coupling between Ampère's law and velocity moments removes the requirement to resolve the electron plasma period without introducing nonlinear iterations. The split subsystems preserve energy, and a fourth-order composition raises temporal accuracy while retaining exact fully discrete mass and total-energy conservation. Analysis establishes unconditional stability. One-dimensional, one-velocity-dimensional tests verify convergence, conservation, and long-time behavior; compared with second-order splitting, the high-order scheme enforces Gauss's law more accurately and maintains better fidelity at large CFL numbers. The current results do not establish exact Gauss-law preservation, and multidimensional or full Vlasov--Maxwell extensions are not demonstrated.

### Contributions

1. Built a high-order SLDG discretization for the Vlasov--Ampère system with no CFL stability restriction.
2. Semi-implicitly coupled fields and distribution moments without requiring nonlinear solves or plasma-period resolution.
3. Preserved mass and total energy exactly at the fully discrete level.
4. Used fourth-order operator composition to obtain high-order accuracy in both space and time.
5. Demonstrated improved Gauss-law enforcement and numerical fidelity over second-order schemes at large CFL numbers.
