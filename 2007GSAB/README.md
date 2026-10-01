# 2007GSAB

## ChatGPT (July 2026)

### Summary

GYSELA evolves the full ion distribution function in a global five-dimensional, electrostatic gyrokinetic model of ion-temperature-gradient turbulence in simplified toroidal geometry. Because a full-$f$ calculation evolves equilibrium and fluctuations together, initialization is consequential. A canonical Maxwellian balances curvature-driven vertical charge separation through parallel flow, whereas a local Maxwellian generates polarization, large-scale electric fields, and sheared flows. Those artificial flows reduce the effective linear growth rate and delay turbulence, although the late nonlinear diffusivities become similar. A nonlinear comparison with the $\delta f$ particle-in-cell code ORB5 gives broadly consistent transport, with remaining differences attributed to boundary conditions, profile relaxation, and self-consistent zonal flows. A scan over $\rho_*$ shows that transport scaling is not a function of system size alone: correlation properties are consistent with gyroBohm behavior at small $\rho_*$ well above threshold and Bohm-like behavior at larger $\rho_*$ near threshold. Finally, a reduced three-dimensional flux-driven model with a constant heat source reaches a statistical steady state while retaining bursty relaxation, large convection cells, zonal flows, and measurable non-Maxwellian moments. These results motivate fully flux-driven five-dimensional studies.

### Contributions

1. Demonstrated global full-$f$ gyrokinetic evolution of the complete ion distribution with the semi-Lagrangian GYSELA code.
2. Showed how non-equilibrium initialization creates sheared flows that suppress linear growth and delay turbulence onset.
3. Nonlinearly benchmarked GYSELA against the independently formulated ORB5 $\delta f$ particle-in-cell code.
4. Found that $\rho_*$ transport scaling depends jointly on system size and distance from the instability threshold.
5. Achieved a flux-driven statistical steady state in a reduced model and characterized its bursty, non-Maxwellian dynamics.
