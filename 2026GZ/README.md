# 2026GZ

## ChatGPT (July 2026)

### Summary

This paper develops a space-time Galerkin time-domain boundary element method for predicting how aircraft surfaces scatter and shield noise from transient, rotating, or broadband sources. The formulation enforces sound-hard boundary conditions and incorporates uniform mean flow through coordinate transformations. Unlike collocation TDBEMs, its Galerkin discretization is unconditionally stable, requires no tuned stabilization parameter, and can represent thin bodies with a single element layer. The principal numerical obstacle--singular double integration over space and time--is handled by decomposing triangle intersections with light-cone boundaries, analytically integrating the radial coordinate, and reducing the remaining inner calculation to one-dimensional quadrature. Sphere, disk, and plane tests cover curved and sharp-edged geometries, closed and thin surfaces, harmonic and transient sources, and media with and without mean flow; all agree closely with analytical solutions, with joint refinement showing second-order accuracy. Coupling the method to RANS/Ffowcs Williams--Hawkings propeller data reproduces measured amplification and shielding trends for trailing-edge-mounted propellers, with most installation-effect discrepancies below $5\,\mathrm{dB}$.

### Contributions

1. Formulated an unconditionally stable space-time Galerkin TDBEM for aeroacoustic scattering without tuned stabilization parameters.
2. Incorporated uniform mean-flow effects through variable transformations without altering the boundary-integral machinery.
3. Reduced singular double space-time integrals to efficient decomposition-based quadrature with analytical radial integration.
4. Validated the method across three analytical cases spanning curved, sharp-edged, closed, thin, stationary-flow, and mean-flow configurations.
5. Coupled the solver to CFD-derived propeller noise and reproduced experimental scattering and shielding trends over plate positions and sizes.
