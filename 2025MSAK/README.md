# 2025MSAK

## ChatGPT (July 2026)

### Summary

Free-boundary tokamak equilibrium calculations must combine plasma currents, external coil fields, limiter geometry, and numerical control of vertical drift. The paper presents pyIPREQ, a Python implementation that solves the axisymmetric Grad--Shafranov equation using Green's functions for boundary fluxes, finite differences in the interior, and Picard iteration for a prescribed toroidal-current profile. It adds limiter-defined plasma boundaries, derived equilibrium quantities, G-EQDSK output, and artificial feedback coils that stabilize iterations for elongated plasmas. A reconstruction mode constrains the magnetic-axis position inferred from diagnostics by optimizing current-profile parameters; an alternate geometric shift improves the vertical constraint. Comparisons with a published ITER equilibrium, the original IPREQ code, and FREEGS show close agreement in flux surfaces and quantities such as safety factor, plasma beta, and internal inductance. ADITYA-U cases demonstrate position-constrained reconstructions and agreement with magnetic-probe measurements, while SST-1 and divertor-coil cases illustrate predictive use. The method is not a full diagnostic reconstruction: results depend on initial profile guesses, the axis and current-density maxima are approximately aligned, and the unoptimized serial Python code is slower than IPREQ.

### Contributions

1. Implemented a free-boundary Grad--Shafranov solver in Python using Green's-function boundary fluxes, finite differences, and self-consistent Picard iteration.
2. Added limiter geometry, equilibrium diagnostics, G-EQDSK export, and feedback-coil stabilization for elongated configurations.
3. Developed an optimization-based method that constrains equilibria to a prescribed magnetic-axis position inferred from measurements.
4. Introduced a vertical current-profile transformation that improves axis alignment when direct parameter optimization is inadequate.
5. Benchmarked the implementation against ITER, IPREQ, and FREEGS results and demonstrated it on ADITYA-U and SST-1 scenarios.
