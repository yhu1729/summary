# 2026LLXZ

## ChatGPT (July 2026)

### Summary

Li et al. accelerate forcing-term evaluation in the Enskog--Vlasov--Shakhov kinetic equation for dense, nonequilibrium fluids. They expand the molecular distribution in Hermite polynomials in a locally shifted and temperature-scaled velocity coordinate, so the Maxwellian is recovered exactly at zeroth order and higher coefficients represent nonequilibrium corrections. A matching shifted-and-scaled Gauss--Hermite quadrature reduces the number of discrete velocities, while a component-wise recurrence avoids full tensor manipulation and supports arbitrary expansion order. Fourier, Couette, and Poiseuille flows validate surface-confinement behavior; equilibrium coexistence and evaporation tests assess phase transitions and interfacial Knudsen layers. The method matches high-resolution finite-difference references with far fewer velocity nodes and larger time steps, reaching a reported 566-fold speedup in a two-dimensional Poiseuille case. An adaptive expansion raises order near interfaces and vapor regions while retaining low order in near-equilibrium liquid.

### Contributions

1. Reformulated the Enskog--Vlasov forcing term through a locally shifted-and-scaled Hermite expansion.
2. Derived component-wise arbitrary-order coefficient formulas that avoid expensive tensor operations.
3. Coupled the expansion to shifted-and-scaled Gauss--Hermite quadrature, reducing velocity nodes by one to two orders of magnitude.
4. Introduced a local adaptive-order criterion that concentrates nonequilibrium corrections near interfaces and Knudsen layers.
5. Validated surface-confined, phase-equilibrium, and evaporative flows, including up to 566-fold speedup over fourth-order velocity-space finite differences.
