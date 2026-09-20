# 2026FPPK

## ChatGPT (July 2026)

### Summary

Stellarator design usually separates plasma-equilibrium optimization from coil design, which can yield attractive plasmas that require impractical coils. This work turns QUADCOIL's winding-surface optimization into a differentiable coil-complexity proxy embedded inside equilibrium optimization. The resulting quasi-single-stage method retains only equilibrium degrees of freedom while representing filament coils, permanent magnets, or dipole arrays and supporting realistic quadratic objectives and constraints. The authors add adjoint differentiation, a JAX-based implementation, and a differentiable winding-surface generator that removes self-intersections while following the plasma boundary. Two studies validate the proxy after discarding the winding-surface solution and cold-starting higher-fidelity coil optimization. For a MUSE-like configuration, the optimized equilibrium needs about $34\%$ fewer permanent magnets at comparable field accuracy. For an ARIES-CS-like configuration, subsequent filament-coil optimization reduces both peak and root-mean-square Lorentz forces by about $30\%$ while preserving geometric constraints. The method provides an inexpensive bridge between conventional two-stage and full single-stage stellarator co-design.

### Contributions

1. Formulated a flexible QUADCOIL-based quasi-single-stage proxy that embeds coil optimization inside equilibrium optimization without explicit coil degrees of freedom.
2. Derived an adjoint differentiation route and implemented end-to-end differentiation in JAX for constrained winding-surface subproblems.
3. Introduced a differentiable winding-surface generator that removes self-intersections and follows changing plasma boundaries.
4. Demonstrated a MUSE-like permanent-magnet design using $34.2\%$ fewer magnets at matched magnetic-field error.
5. Demonstrated an ARIES-CS-like filament-coil design with roughly $30\%$ lower peak and rms forces while retaining geometric constraints.
