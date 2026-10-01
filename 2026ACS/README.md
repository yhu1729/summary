# 2026ACS

## ChatGPT (July 2026)

### Summary

This survey presents exponential Runge--Kutta methods as schemes for semilinear problems $u'=Au+g(t,u)$ that propagate the stiff linear component through matrix exponentials and approximate the nonlinear variation-of-constants integral with Runge--Kutta-like stages and $\varphi$-functions. It develops the basic construction, consistency, stability, and order framework before tracing more than sixty years of work from early exponential formulas through Krylov and contour methods, stiff order conditions, exponential Rosenbrock methods, parallel and multirate schemes, delay equations, and recent structure-preserving applications. The review emphasizes that practical performance depends on efficiently computing matrix-function actions and on whether stiffness is concentrated in the linear operator. Three deliberately didactic examples compare second- and fourth-order exponential, classical Runge--Kutta, and Rosenbrock schemes on a scalar stiff problem, a Duffing oscillator, and a pseudospectral delay-equation system. The experiments illustrate substantial stability and accuracy advantages in suitable stiff settings but are not a comprehensive benchmark. The numerical section covers explicit exponential methods; implicit variants and broader robustness studies remain open.

### Contributions

1. Gave a self-contained derivation of exponential Runge--Kutta schemes from variation of constants and explained the role of matrix exponentials and $\varphi$-functions.
2. Reconstructed the field's historical development from the late 1950s through modern stiff-order, high-order, parallel, and multirate methods.
3. Synthesized practical matrix-function techniques, including scaling and squaring, Krylov, interpolation, and contour-integral approaches.
4. Surveyed applications and theory for partial differential equations, delay equations, advection--diffusion--reaction systems, order reduction, and structure preservation.
5. Supplied three didactic comparisons against classical Runge--Kutta and Rosenbrock methods, clarifying when explicit exponential schemes gain stability or accuracy and when overhead dominates.
