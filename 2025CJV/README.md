# 2025CJV

## ChatGPT (July 2026)

### Summary

This paper analyzes Anderson acceleration by rewriting the discrete method as an adaptive multistep momentum scheme and taking a high-resolution continuous-time limit. The resulting second-order ODE has variable effective mass, which gives a physical explanation for a known failure mode of standard Anderson acceleration: unchecked mass growth acts like negative damping and injects energy into stiff nonlinear iterations. The same high-resolution expansion also exposes an implicit Hessian-driven damping term that can stabilize high-curvature directions. Building on this interpretation, the authors propose Energy-Guarded Anderson Acceleration, which bounds mass growth and enforces energy dissipation. Their convergence analysis uses an acceleration-gain factor to show that the guarded method preserves useful geometric contraction while suppressing nonlinear approximation error. Numerical tests on ill-conditioned convex composite problems show better stability and convergence than standard Anderson mixing and Nesterov acceleration. The paper frames acceleration as a balance between inertial gain and thermodynamic consistency.

### Contributions

1. Recast Anderson acceleration as an adaptive momentum method.
2. Derived a high-resolution variable-mass ODE limit for Anderson acceleration.
3. Identified effective-mass growth as a negative-damping instability mechanism.
4. Proposed Energy-Guarded Anderson Acceleration to enforce dissipative dynamics.
5. Supported the theory with convergence analysis and ill-conditioned optimization experiments.
