# 2026HGW

## ChatGPT (July 2026)

### Summary

This paper develops computable a posteriori error control for the integrating factor midpoint method applied to linear second-order evolution equations, including wave-type problems $u''+Au=f$ with a positive self-adjoint operator $A$. A continuous piecewise-linear approximation first yields residual-based bounds that are suboptimal in time. The authors then construct a continuous piecewise-quadratic reconstruction and use an energy argument to recover optimal-order bounds in $L^\infty$-in-time and energy-in-space norms for both displacement and velocity. Because the estimators depend on the discrete solution and problem data, they support an adaptive step-size algorithm without requiring specialized evaluation of matrix-exponential actions. Four numerical examples confirm second-order convergence of the reconstructed estimator and show that the controller refines near localized temporal features and coarsens elsewhere. The analysis assumes a linear problem whose first-order operator generates a bounded $C_0$ semigroup; extensions to nonlinear equations are not established.

### Contributions

1. Derived residual-based a posteriori bounds for an integrating factor midpoint discretization of second-order evolution equations.
2. Identified the loss of optimal order caused by the direct piecewise-linear approximation.
3. Introduced a quadratic time reconstruction that restores optimal-order error estimates.
4. Converted the reliable estimator into an adaptive time-step acceptance and update strategy.
5. Demonstrated convergence and localized refinement on smooth and sharply varying wave-type tests.
