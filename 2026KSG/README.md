# 2026KSG

## ChatGPT (July 2026)

### Summary

T3FF is an open-source C++ code for isothermal, three-dimensional
electromagnetic gyrofluid simulations of tokamak-edge drift--Alfvén turbulence.
Its full-$f$ formulation permits finite-amplitude density fluctuations, while
its full-$k$ polarization retains second-order Padé finite-Larmor-radius
effects beyond the usual long-wavelength approximation. The present version
uses a field-aligned flux tube in simplified circular toroidal geometry with
resistive parallel dynamics. Perpendicular advection is discretized with an
Arakawa scheme, time evolution uses Adams--Bashforth stepping, and polarization,
Ampère, and gyroaveraging equations are handled by iterative and FFT-based
solvers with OpenMP parallelism. Verification includes recovery of a published
edge-turbulence benchmark in the delta-$f$ limit, parallel and perpendicular
grid-convergence studies, and sound- and Alfvén-wave tests. Electromagnetic
beta scans reproduce transport reduction from magnetic-flutter damping followed
by transition to a resistive ballooning regime. The paper is a code-reference
study; steep-gradient non-Boussinesq applications, scrape-off-layer boundaries,
and a thermal six-moment extension remain future work.

### Contributions

1. Introduced a three-dimensional full-$f$, full-$k$ electromagnetic gyrofluid model and reference implementation.
2. Combined field-aligned toroidal geometry with consistent finite-Larmor-radius polarization and resistive parallel dynamics.
3. Documented the finite-difference, Arakawa, FFT, iterative-solver, and OpenMP implementation.
4. Verified delta-$f$ benchmark recovery, spatial convergence, and sound- and Alfvén-wave dynamics.
5. Demonstrated beta-dependent magnetic-flutter damping and the transition to resistive ballooning transport.
