# 2026RS

## ChatGPT (July 2026)

### Summary

This paper develops an asymptotic-preserving finite-volume solver for
Boltzmann kinetic equations using a micro--macro decomposition. The
distribution is separated into an equilibrium component represented by
macroscopic moments and a nonequilibrium component retained on a velocity
grid, reducing velocity-domain requirements near equilibrium. The work extends
earlier one-dimensional BGK schemes to two spatial and two velocity dimensions,
the transport-correct ES-BGK collision operator, and diffusely reflecting
walls. The macro equations use kinetic flux-vector splitting and receive heat
flux from the micro distribution; the projected micro equation uses upwind
transport. L-stable implicit collision updates and operator splitting preserve
stability as the Knudsen number tends to zero. Manufactured solutions establish
convergence in one and two dimensions, while shock tubes, cylindrical shocks,
wall-driven flow, and a lid-driven cavity exercise continuum through
rarefied-flow regimes. An open-source C++/MPI implementation achieves about
$74\%$ weak-scaling efficiency at the largest reported processor count and
favorable strong scaling for the fixed test problem.

### Contributions

1. Extended micro--macro kinetic discretization to multidimensional ES-BGK dynamics.
2. Coupled kinetic flux-vector-split macro updates to projected upwind micro updates through nonequilibrium heat flux.
3. Derived compatible diffusely reflecting boundary conditions for both components.
4. Verified asymptotic-preserving behavior and convergence on one- and two-dimensional kinetic benchmarks.
5. Implemented and evaluated a parallel C++/MPI solver with weak- and strong-scaling studies.
