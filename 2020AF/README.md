# 2020AF

## ChatGPT (August 2026)

### Summary

FastRK3 is an explicit pressure-correction projection method for incompressible Navier--Stokes flows on orthogonal curvilinear grids. It combines a three-stage Runge--Kutta update with extrapolated intermediate pressure gradients, so the pressure Poisson problem is solved only at the final stage. Expressing the operators in orthogonal coordinates removes cross-derivatives and yields Cartesian-like seven-point stencils. When the metric factors are invariant in one direction, FastPoc applies an FFT in that direction and direct sparse factorization to independent two-dimensional systems. Verification against standard RK3, Blasius and Jeffery--Hamel solutions shows near-identical results and approximately second-order spatial accuracy; lid-driven polar-cavity results agree with experiments. On the tested grids, FastPoc is 30--60 times faster than hypre SMG at divergence tolerances from $10^{-6}$ to $10^{-12}$, and the complete solver is 4--7 times faster. Applications reproduce attached and separated laminar flow over ramp and Gaussian-bump geometries. FastPoc requires orthogonal grids with metric coefficients invariant in one coordinate, and its direct factorizations can consume substantial memory.

### Contributions

1. Formulated the velocity-based incompressible Navier--Stokes equations in general orthogonal curvilinear coordinates, including curved-wall and outflow boundary treatments.
2. Introduced FastRK3, which extrapolates intermediate pressure gradients and requires only one pressure Poisson solve per time step.
3. Developed FastPoc, an FFT/direct sparse solver for orthogonal grids whose metric coefficients are invariant in one coordinate direction.
4. Verified approximately second-order spatial accuracy using analytical solutions and comparisons with standard RK3 and polar-cavity experiments.
5. Demonstrated 30--60-fold Poisson-solver and 4--7-fold full-solver speedups on the tested systems, then applied the method to ramp and bump flows.
