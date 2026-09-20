# 2026GTCD

## ChatGPT (July 2026)

### Summary

The paper introduces PICSL, a fully implicit semi-Lagrangian integrator that applies BDF2 consistently to spherical shallow-water dynamics and trajectory equations, solving the coupled nonlinear system by Picard iteration with convergence-based stopping. Analysis establishes second-order temporal accuracy, A-stability for the dynamics, absence of the spurious BDF2 resonance that affects centered Crank--Nicolson semi-Lagrangian schemes, and favorable Rossby- and gravity-wave dispersion. The time step is not Courant-limited by the dynamics, although fixed-point trajectory convergence requires a Lipschitz condition in regions with strong velocity gradients. Steady geostrophic flow, Rossby--Haurwitz waves, isolated topography, barotropic instability, and realistic-orography tests confirm second-order convergence, suppress terrain-induced noise without off-centering or filtering, and generally improve energy and potential-enstrophy preservation relative to centered or off-centered CNSL. Costs are comparable in most cases, but semi-Lagrangian advection is more expensive because PICSL traces midpoint and departure trajectories. Evaluation in three-dimensional operational GEM configurations remains future work.

### Contributions

1. Defined a fully implicit BDF2 semi-Lagrangian scheme with Picard nonlinear solves and tolerance-based stopping.
2. Applied BDF2 consistently to governing dynamics and kinematic trajectories, removing a source of semi-Lagrangian inconsistency.
3. Established second-order accuracy, A-stability, and absence of spurious BDF2 resonance without off-centering or filtering.
4. Derived Rossby- and gravity-wave dispersion behavior and the trajectory Lipschitz convergence restriction.
5. Demonstrated reduced terrain noise and improved invariant preservation on spherical shallow-water benchmarks at costs comparable to CNSL in most cases.
