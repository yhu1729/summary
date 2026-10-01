# 2026LYZR

## ChatGPT (July 2026)

### Summary

This work develops a second-order semi-implicit integrator for the multispecies linearized Sugama collision operator used in gyrokinetic tokamak simulations. The scheme treats the collision operator as a unified update rather than splitting its test- and field-particle components. It advances stiff isothermal pitch-angle scattering and energy diffusion implicitly with a trapezoidal rule, while treating the non-isothermal model and field-particle terms explicitly. Combined with a finite-volume discretization in $(v_\parallel,\mu)$, this produces independent sparse or banded solves for each species instead of a fully implicit cross-species system. Implemented in the NLT code, the method permits time steps tens to thousands of times larger than explicit integration in electron and multispecies relaxation tests. It preserves particle number to machine precision and, with the complete correction terms, also preserves total momentum and energy, maintains adjointness, and satisfies the $H$-theorem. Neoclassical ion-energy flux and bootstrap-current profiles agree with GENE and ORB5. Positivity is not guaranteed intrinsically, and the tested global case omits kinetic electrons, equilibrium electric field, and sources.

### Contributions

1. Constructed a second-order semi-implicit update without splitting the physical collision operator.
2. Isolated the stiff test-particle terms while avoiding fully implicit cross-species coupling.
3. Coupled the integrator to a conservative finite-volume velocity-space discretization.
4. Demonstrated large stable-time-step gains while retaining conservation and entropy production.
5. Validated the NLT implementation against independent neoclassical transport codes.
