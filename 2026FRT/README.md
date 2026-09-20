# 2026FRT

## ChatGPT (July 2026)

### Summary

This work proposes an asymptotic-preserving modified Crank--Nicolson particle pusher for two-dimensional Vlasov--Poisson dynamics under a strong, spatially varying magnetic field of fixed direction. Standard Crank--Nicolson variants lose consistency when the Larmor scale is unresolved. The new formulation augments particle position and velocity with kinetic energy and an effective magnetic-gradient force, allowing time steps independent of the small magnetization parameter while filtering fast gyromotion. Under boundedness assumptions, the authors prove convergence at fixed step size to a second-order discrete guiding-center system and second-order behavior of limiting energy and magnetic moment. Particle-in-cell tests for single trajectories, diocotron instability, and merging D-shaped vortices reproduce slow drift, confinement, energy exchange, and asymptotic reference densities over long times. The method is substantially more accurate than the compared IMEX scheme but costs more than twice as much in reported tests. Its analysis assumes stability rather than proving it, positivity of the auxiliary energy is not guaranteed, large steps do not resolve the physical gyrofrequency, and extension to three-dimensional curvature and parallel motion remains open.

### Contributions

1. Diagnosed the strong-field inconsistency of conventional Crank--Nicolson particle pushers.
2. Added kinetic energy and a magnetic-gradient force to restore uniform consistency.
3. Proved convergence to a second-order discrete guiding-center limit.
4. Filtered unresolved fast scales without a magnetization-dependent time-step restriction.
5. Validated long-time behavior in self-consistent particle-in-cell plasma tests.
