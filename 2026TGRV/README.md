# 2026TGRV

## ChatGPT (July 2026)

### Summary

Coupled three-dimensional--one-dimensional transport models represent solute exchange between a bulk domain and a thin embedded structure without resolving the structure as a full three-dimensional region. The paper defines a fully discrete approximation that combines a conforming finite-element method for the three-dimensional concentration with an interior-penalty discontinuous Galerkin method for the one-dimensional concentration. The coupling transfers solute between the two discrete domains while allowing their mesh sizes to be chosen independently. Assuming sufficient regularity of the weak solution, the authors derive error estimates for both concentrations. The bounds are optimal with respect to the time-step size and the respective three- and one-dimensional mesh sizes under the stated assumptions. Numerical convergence experiments support the theoretical rates. The results provide a rigorous accuracy foundation for mixed-dimensional transport calculations; their guarantees remain conditional on the solution regularity and model assumptions used in the analysis.

### Contributions

1. Defined a coupled discretization for time-dependent three-dimensional--one-dimensional solute transport.
2. Combined conforming finite elements in the bulk domain with interior-penalty discontinuous Galerkin approximation on the embedded line.
3. Derived simultaneous error bounds for the three-dimensional and one-dimensional concentrations.
4. Proved optimal dependence of the estimates on the time step and both spatial mesh sizes under sufficient regularity.
5. Verified the theoretical convergence behavior through numerical experiments.
