# 2025BKKS

## ChatGPT (July 2026)

### Summary

Grid-based low-rank approximation of multivariate functions can require constructing a large tensor before compression. This paper introduces a mesh-free, two-level Chebyshev--Tucker representation. It samples the target only at a moderate tensor product of Chebyshev nodes, forms the coefficient tensor, and compresses that tensor with Tucker alternating least squares. Discretized Chebyshev basis functions then transfer the result to an arbitrarily fine grid without repeating the rank optimization. The Tucker ranks can be much smaller than the interpolation degree and approach those obtained by applying Tucker decomposition directly to the full grid. Error and complexity estimates relate interpolation accuracy, coefficient compression, and the final approximation. For functions with singularities, the method targets the smooth long-range component supplied by a range-separated tensor representation. Tests on biomolecular electrostatic potentials and monopole/dipole lattice systems show controllable accuracy, weak dependence on particle count, and quasi-optimal ranks. Extensions to higher dimensions require other hierarchical tensor formats to avoid dimensional growth.

### Contributions

1. Introduced a mesh-free hybrid Chebyshev--Tucker format for multivariate function approximation.
2. Separated function sampling and rank optimization from final-grid resolution.
3. Derived error and complexity estimates for the two-level construction.
4. Extended the method to long-range components of singular many-particle potentials in range-separated form.
5. Demonstrated quasi-optimal ranks and controllable accuracy for biomolecular and lattice electrostatics.
