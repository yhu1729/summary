# 2025HBS

## ChatGPT (July 2026)

### Summary

Resolving particle gyromotion inside an MHD domain creates a severe scale separation. The MHD-gPIC module in Athena++ instead advances energetic particles with guiding-center equations while representing the thermal component as magnetohydrodynamic fluid. Carefully derived momentum and energy source terms couple particle feedback to the fluid and permit a non-negligible nonthermal fraction. A correction to the guiding-center momentum equation restores Galilean invariance, which is important for particle confinement in moving plasmoids, while including perpendicular particle pressure in the fluid pressure lets the Riemann solver suppress gradient noise. The second-order implementation supports static and adaptive mesh refinement, parallel load balancing, and adds about 10--18% per-particle overhead relative to MHD-PIC. Benchmarks validate trajectories, feedback, and wave behavior. Preliminary reconnection simulations find mainly Fermi acceleration, pressure anisotropy, and strong feedback from energetic ions. The guiding-center approximation excludes gyro-resonant and sub-grid scattering effects, defining the method's intended regime.

### Contributions

1. Formulated and implemented an MHD--guiding-center-PIC method in Athena++ for multiscale plasma simulations.
2. Added a Galilean-invariant guiding-center momentum correction that improves confinement in moving structures.
3. Derived backreaction terms valid when energetic particles form a non-negligible plasma fraction.
4. Reduced particle-pressure noise by incorporating perpendicular particle pressure into the fluid Riemann solve.
5. Validated the coupled implementation and demonstrated particle acceleration with feedback in magnetic reconnection.
