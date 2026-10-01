# 2026LG

## ChatGPT (July 2026)

### Summary

The paper accelerates a discrete unified gas kinetic scheme for strongly inhomogeneous nanoscale fluids whose kinetic model contains costly nonlocal-gradient, weighted-density, and mean-field-potential integrals. It replaces direct integral evaluation with finite-difference nonlocal gradients, adaptive volume averaging, and coarser distance-dependent sampling of rapidly decaying attractive interactions. These changes reduce complexity from $O(NN_\sigma)$ to $O(N)$, where $N$ is the number of physical cells and $N_\sigma$ is the integration-domain size. Static density structures and force-driven slit flows agree with Monte Carlo, molecular-dynamics, and original-scheme results, while two-dimensional tests achieve speedups of up to two orders of magnitude. The efficient scheme enables previously impractical two-dimensional applications. Pressure-driven channel simulations show that pressure and body-force driving are generally inequivalent at the nanoscale because the streamwise density profile is nonlinear. Square-duct simulations reveal wall adsorption, corner density peaks, and weakening of the Knudsen minimum as the duct narrows.

### Contributions

1. Reduced nonlocal kinetic-scheme complexity from $O(NN_\sigma)$ to $O(N)$.
2. Replaced integral nonlocal gradients with an efficient finite-difference construction.
3. Added adaptive volume averaging and distance-coarsened mean-field evaluation.
4. Matched reference methods while attaining up to two orders of magnitude speedup.
5. Resolved inequivalent nanoscale driving and square-duct corner density accumulation.
