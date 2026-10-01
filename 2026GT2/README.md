# 2026GT2

## ChatGPT (September 2026)

### Summary

The paper develops a first-order implicit--explicit method for nonequilibrium gray radiation hydrodynamics that preserves the model's physically admissible set. The coupled compressible-fluid and radiation system is split into two hyperbolic subsystems and one stiff parabolic radiation-diffusion subsystem. Graph-based finite element updates and derived local wave-speed bounds make each hyperbolic stage invariant-domain preserving. The parabolic stage uses backward Euler, a Picard iteration, and local Newton solves for radiation energy and material temperature; its admissibility proof holds under mild equation-of-state and spatial-discretization assumptions and does not depend on the Picard stopping tolerance. The composed approximation is shown to be consistent, conservative, invariant-domain preserving, and first-order accurate. Numerical experiments confirm convergence and robustness, including regimes with strongly contrasted opacity and high Mach number. The construction is deliberately a low-order foundation for a subsequent high-order method, where limiting can blend high-order states toward these admissible low-order updates.

### Contributions

1. Introduced a three-part split of gray radiation hydrodynamics into two hyperbolic and one parabolic subsystem.
2. Derived the maximum wave speed needed for invariant-domain preservation in the second hyperbolic stage.
3. Constructed conservative graph-based finite element updates that preserve the admissible thermodynamic domain.
4. Designed a robust implicit radiation solve using Picard iteration and local Newton updates.
5. Proved first-order consistency, conservation, and admissibility and confirmed the predicted convergence numerically.
