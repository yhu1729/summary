# 2026FJW

## ChatGPT (July 2026)

### Summary

Fu, Jiang, and Wang construct an oscillation-free energy-based discontinuous Galerkin method for second-order wave equations with nonsmooth solutions. Standard EDG fluxes and derivative-based damping cannot move piecewise-constant data whose jumps coincide with element interfaces, so the authors add a solution-jump penalty alongside projection-based adaptive damping. The penalty restores the correct wave propagation, while damping suppresses Gibbs-type oscillations; their mesh scaling preserves high-order behavior in smooth regions. Semi-discrete energy stability and a priori error estimates are proved in one and multiple dimensions for general numerical fluxes. Tests with smooth linear and semilinear waves attain optimal convergence for alternating and Sommerfeld fluxes, while nonsmooth linear, Dirac-source, Sine--Gordon, and Klein--Gordon problems show accurate wave speeds and non-oscillatory profiles. The analysis is restricted mainly to Cartesian meshes and periodic conditions, and nonlinear experiments without exact solutions use fine-grid finite differences as references.

### Contributions

1. Extended energy-based discontinuous Galerkin methods to nonsmooth second-order wave solutions using complementary damping and jump-penalty terms.
2. Identified why derivative-only formulations can freeze discontinuous piecewise-constant initial data.
3. Established semi-discrete energy dissipation for general flux parameters in one and multiple dimensions.
4. Derived a priori energy-norm error estimates showing that stabilization retains high-order smooth-solution accuracy.
5. Demonstrated robustness on linear discontinuities, distributional sources, and nonlinear Sine--Gordon and Klein--Gordon equations in one and two dimensions.
