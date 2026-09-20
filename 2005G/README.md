# 2005G

## ChatGPT (August 2026)

### Summary

Strong stability preserving (SSP) time integrators are designed for method-of-lines systems $\dot u=L(u)$ whose forward Euler step is nonlinearly stable in a norm, seminorm, or convex functional under $\Delta t\le\Delta t_{\mathrm{FE}}$. This review explains how a Runge--Kutta or multistep method written as convex combinations of forward Euler steps inherits that property under $\Delta t\le c\Delta t_{\mathrm{FE}}$, with downwind spatial operators needed when coefficients are negative. It catalogs efficient explicit SSP Runge--Kutta schemes for nonlinear and linear constant-coefficient problems, including low-storage implementations, order barriers, effective CFL measures, and the need for stable intermediate stages. Explicit and implicit multistep methods are assessed; higher-order methods generally face restrictive coefficients, while suitable starting procedures can relax boundedness requirements. The paper also shows why higher-order implicit SSP methods are not unconditionally stable and are often not cost-effective. Finally, it connects the optimal SSP CFL coefficient of a Runge--Kutta method to its radius of absolute monotonicity, providing a constructive route from Butcher coefficients to an optimal Shu--Osher representation.

### Contributions

1. Presented the Shu--Osher convex-decomposition argument that transfers forward-Euler strong stability to higher-order Runge--Kutta methods under an explicit CFL coefficient.
2. Collected optimal nonlinear SSP schemes, including low-storage variants and a five-stage fourth-order method with coefficient $c=1.508$.
3. Treated linear constant-coefficient problems separately, giving higher-order method families, effective CFL comparisons, and coefficient bounds.
4. Demonstrated why SSP behavior is needed at intermediate stages and surveyed restrictive results for explicit and implicit multistep and Runge--Kutta methods.
5. Connected the optimal SSP coefficient to the radius of absolute monotonicity and constructed an optimal Shu--Osher representation from Butcher data.
