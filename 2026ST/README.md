# 2026ST

## ChatGPT (July 2026)

### Summary

This paper compares explicit integrators for obstacle-potential phase-field models coupled to concentration diffusion. It treats forward Euler, strong-stability-preserving Runge--Kutta schemes, and first- and second-order Runge--Kutta--Legendre super-time-stepping methods. The implementation projects every phase-field stage onto the Gibbs simplex, adapts error estimates to compact-support phase storage, and uses a PID-type step controller. Rather than comparing only with refined numerical references, the authors construct equilibrium and kinetic benchmarks with sharp-interface solutions, allowing temporal, spatial, and diffuse-interface errors to be separated. Across practical resolutions, spatial and interface-width errors usually dominate time-integration error; strict discrete energy stability has little effect on the sharp-interface error in the tested cases. Super-time-stepping is therefore substantially more efficient than forward Euler without appreciable accuracy loss. Three-dimensional grain-growth examples reproduce unpinned growth, Zener-like limiting behavior from immobile particles, and slowed continued growth from mobile pores that move and merge. The largest gain occurs when diffusion creates strongly separated time scales.

### Contributions

1. Defined reproducible equilibrium and kinetic phase-field benchmarks with analytical sharp-interface solutions.
2. Adapted strong-stability-preserving and Runge--Kutta--Legendre schemes to simplex-constrained, compactly stored phase fields.
3. Developed field-aware error estimation and PID-controlled adaptive stepping for coupled phase and concentration variables.
4. Separated temporal, spatial, and interface-width errors and evaluated the practical role of energy stability.
5. Demonstrated the methods on three-dimensional grain growth with no particles, immobile pinning particles, and mobile coalescing pores.
