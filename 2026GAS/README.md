# 2026GAS

## ChatGPT (July 2026)

### Summary

This work extends kinetic-based regularization (KBR), a localized one-parameter kernel regression method, to spatial-derivative estimation. An improved correction makes the local quadratic fit second-order accurate away from training points. An explicit scheme extracts derivatives from closed-form fitted coefficients; an implicit scheme perturbs a query point and solves a small local system. On one-dimensional Camel and Rastrigin functions, explicit extraction is more stable for clean unseen data, while implicit extraction is more robust to noise. Clean-data tests outperform a differential-neural-network baseline and compare favorably with nonuniform finite differences. A preliminary two-dimensional example recovers gradients and Hessians. KBR is also inserted into conservative solvers through interface-flux prediction for inviscid Burgers and Sod shock-tube problems. MacCormack- and Roe-based variants remain stable and preserve conservative structure, although the Burgers solution exhibits Gibbs oscillations and irregular high-dimensional point clouds remain future work.

### Contributions

1. Corrected KBR's local quadratic reconstruction to attain the intended accuracy at unseen query points.
2. Derived explicit and implicit procedures for extracting gradients and second derivatives.
3. Characterized complementary behavior: stronger clean-data stability for the explicit scheme and greater noise robustness for the implicit scheme.
4. Demonstrated preliminary two-dimensional gradient and Hessian recovery.
5. Integrated KBR interface-flux predictions into conservative MacCormack and Roe shock-capturing solvers.
