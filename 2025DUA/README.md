# 2025DUA

## ChatGPT (July 2026)

### Summary

The viscous Burgers equation couples nonlinear advection with diffusion and develops increasingly sharp fronts as viscosity decreases. This paper constructs a collocation method that uses B-splines in both independent variables: quadratic B-splines first integrate the equation in time, after which cubic B-splines discretize the resulting spatial problem. Collocation and the boundary conditions reduce each update to a recursive algebraic system for the spline coefficients. Two one-dimensional benchmarks with analytical solutions test shock-like and traveling-front propagation. The reported $L_\infty$ and $L_2$ errors generally decrease as equal time and space increments are refined, and the computed profiles become smoother. Accuracy deteriorates for lower viscosity and near the steep front at the right boundary; the second benchmark retains substantial maximum errors even on the finest tested grid. The study therefore demonstrates the feasibility of a time--space spline construction, but it does not provide a formal stability or convergence analysis. The authors identify higher-order splines in time and space as the next route for improving accuracy.

### Contributions

1. Formulated a Burgers-equation integrator that uses B-spline collocation in both time and space.
2. Combined quadratic temporal splines with cubic spatial splines in a sequential discretization.
3. Derived the recursive coefficient system, including initialization and boundary treatment.
4. Tested the method on analytical shock-wave and traveling-front solutions across multiple viscosities and grid increments.
5. Quantified the loss of accuracy for sharper low-viscosity fronts and identified higher-order splines as a concrete extension.
