# 2026FHDM

## ChatGPT (July 2026)

### Summary

This paper generalizes a gridless quasistatic algorithm for axisymmetric plasma wakes and implements it in Wake-T. Background plasma macroparticles are advanced on radial trajectories, while fields are reconstructed directly from enclosed charge and current rather than deposited onto a fixed plasma grid. The formulation supports arbitrary radial density profiles, multiple mobile plasma species, nonuniform sampling, laser drivers, and particle beams. Independent adaptive grids remain available for the laser envelope and beam pushers, allowing very narrow witness beams to be resolved without globally refining the plasma representation. Benchmarks against FBPIC and HiPACE++ cover laser- and beam-driven wakes, ion motion, beam loading, and tailored local refinement. In the reported laser case, comparable convergence requires roughly $40$ times less combined resolution and reduces runtime from $9.8$ GPU-hours on an A100 to about seven minutes on one CPU core. The approach assumes axial symmetry and the quasistatic approximation, so asymmetric and rapidly evolving phenomena remain outside its scope.

### Contributions

1. Generalized gridless quasistatic wake modeling to arbitrary profiles and multiple plasma species.
2. Coupled the model in Wake-T to laser-envelope and particle-beam solvers.
3. Enabled independent local refinement around narrow beams without a global plasma grid.
4. Benchmarked laser wakes, beam wakes, ion motion, and beam loading against established codes.
5. Demonstrated large resolution and runtime reductions for converged axisymmetric simulations.
