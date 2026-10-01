# 2026CDGV

## ChatGPT (July 2026)

### Summary

The paper proves polynomial-degree-robust convergence properties for an $h$-adaptive conforming finite element method for the Poisson equation in two or three dimensions. Its vertex-patch algorithm uses equilibrated-flux error indicators, Dörfler marking, local residual liftings, and a bounded sequence of newest-vertex bisections. An a posteriori computable criterion controls error contraction; when satisfied, the contraction factor is independent of the fixed polynomial degree $p$. The authors establish discrete reliability with a $p$-independent constant using a recent robust projector. For piecewise-polynomial right-hand sides, this combines with robust estimator efficiency to give a $p$-independent upper threshold for the Dörfler parameter and optimal algebraic convergence rates, although rate-dependent constants and conditional contraction robustness remain. Tests on L-shaped and cross-shaped domains for $p=1,\ldots,4$ attain the expected $\mathrm{DoF}^{-p/2}$ behavior. The computable lower-bound constants stay below $1.6$ and generally require only one local refinement, supporting the criterion's practicality.

### Contributions

1. Designed a fixed-$p$, vertex-based adaptive FEM driven directly by equilibrated-flux estimators.
2. Derived an a posteriori verifiable condition for $p$-robust contraction at every adaptive step.
3. Proved $p$-robust discrete reliability using a polynomial-degree-robust projector.
4. Established optimal algebraic rates under a $p$-independent Dörfler-marking threshold.
5. Confirmed optimal rates, robust estimator effectivity, and small contraction constants numerically.
