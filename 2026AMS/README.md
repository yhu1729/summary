# 2026AMS

## ChatGPT (July 2026)

### Summary

Linear thermo-poroelasticity couples solid displacement, fluid pressure, and temperature, making fully implicit time steps expensive. This paper introduces half-decoupled and fully decoupled first-order schemes that solve the three component equations sequentially. Selected coupling terms are lagged by one time step, allowing the methods to be interpreted as implicit Euler discretizations of related delay equations. The authors prove an abstract first-order error estimate for parabolic delay problems and transfer it to the coupled system. Convergence is guaranteed by weak-coupling conditions expressed only through material and operator constants, rather than a time-step restriction. Finite-element experiments on geothermal-type and manufactured problems confirm first-order convergence when these computable conditions hold, explore their sharpness, and compare the methods with stabilized iterative splittings. The new schemes avoid inner coupling iterations and larger monolithic matrices, but their guarantee depends on sufficiently weak physical coupling.

### Contributions

1. Introduced partially and fully sequential time-stepping schemes for linear thermo-poroelasticity.
2. Reduced each time step to separate mechanics, flow, and heat solves without inner iterations.
3. Recast the lagged schemes as implicit Euler methods for parabolic delay equations.
4. Proved first-order convergence under a priori material-parameter coupling conditions.
5. Numerically assessed convergence, condition sharpness, and performance relative to existing decouplings.
