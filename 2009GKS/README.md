# 2009GKS

## ChatGPT (August 2026)

### Summary

This review updates SSP theory for nonlinear hyperbolic PDEs with discontinuities. An SSP method transfers any forward-Euler stability bound in a norm, seminorm, or convex functional to a higher-order time discretization under a computable step restriction. Burgers, linear-advection/WENO, and near-vacuum Euler tests show that A-, L-, or linearly stable non-SSP integrators can develop oscillations or lose positivity even when SSP schemes remain well behaved at comparable cost. The paper identifies the SSP coefficient with the radius of absolute monotonicity, making it a necessary as well as sufficient worst-case bound, and summarizes stage and order barriers for Runge--Kutta, multistep, and general linear methods. It catalogs optimal or best-known explicit and implicit schemes, emphasizing low-storage explicit Runge--Kutta methods and multistep methods with controlled starts; implicit SSP methods rarely justify their solve cost. Spectral deferred-correction schemes are recast as Runge--Kutta methods, simplifying their optimization and showing that high-order SSP variants require downwinding. The review closes by identifying higher-order general linear and implicit--explicit SSP methods as open directions.

### Contributions

1. Demonstrated practical SSP necessity through examples where conventional linear or implicit stability does not prevent oscillations or loss of positivity.
2. Established the optimal SSP coefficient as the radius of absolute monotonicity, making the bound necessary and sufficient in the stated worst-case setting.
3. Synthesized stage, order, and step-size barriers for explicit and implicit Runge--Kutta, multistep, and general linear methods.
4. Collected optimal or best-known schemes and highlighted efficient low-storage constructions, including a ten-stage fourth-order method with $c=6$.
5. Recast spectral deferred-correction formulas as Runge--Kutta methods and derived downwinding requirements for higher-order variants.
