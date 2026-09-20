# 2026ACKM

## ChatGPT (July 2026)

### Summary

Conservative formulations select physically relevant weak solutions of hyperbolic conservation laws, whereas primitive-variable formulations can simplify wave treatment but may converge to incorrect shock solutions. The paper combines both representations in second-order dual-formulation finite-volume methods for one and two dimensions. Cell averages of conserved and primitive variables evolve on overlapping staggered meshes. A path-conservative central-upwind scheme advances the nonconservative primitive system, and those values provide simple fluxes for the conservative update. Because the two evolutions are otherwise independent, a conservative post-processing step couples them after each timestep, suppresses spurious oscillations, and recovers the correct weak solution. The two-dimensional construction uses separate staggered primitive grids in each coordinate direction and dimension-by-dimension post-processing; several updates can be parallelized. Euler-equation tests recover second-order convergence for a smooth vortex and handle shock tubes, near-vacuum rarefactions, shock--turbulence interaction, blast waves, and multidimensional Riemann problems. In one-dimensional comparisons, the method generally resolves features at least as well as, and often better than, a central scheme on overlapping cells. The current approach remains second order: extending it requires a uniformly accurate higher-order conservative post-processing procedure.

### Contributions

1. Introduced second-order dual-formulation finite-volume methods that evolve conservative and primitive variables on overlapping staggered meshes.
2. Coupled a path-conservative central-upwind primitive update to a conservative update with unusually simple numerical fluxes.
3. Designed conservative post-processing that suppresses oscillations and prevents convergence to nonphysical weak solutions.
4. Extended the framework from one dimension to two using directional primitive grids and dimension-by-dimension coupling.
5. Verified second-order accuracy and robust shock resolution across eight Euler benchmarks, including near-vacuum and multidimensional flows.
