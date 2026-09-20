# 2023ATF

## ChatGPT (August 2026)

### Summary

This paper supplies the theoretical and numerical temporal-accuracy analysis missing from the original FastRK3 work. FastRK3 replaces the intermediate pressure projections of standard three-stage RK3 with a two-level linear extrapolation of pseudo-pressure and retains one pressure Poisson solve per step. By comparing stage errors with standard RK3, the authors show that final velocity retains third-order global accuracy for non-stiff flows when the RK coefficients satisfy a product condition and the extrapolation errors cancel. They derive the general $s$-stage constraint and the $\alpha$--$\beta$ relation; for the chosen RK3 scheme it becomes $\beta=-2\alpha/3+5/6$. Taylor--Green vortex tests confirm that midpoint and standard-approximation extrapolations give third-order velocity and second-order pressure with periodic or unsteady Dirichlet boundaries, whereas endpoint extrapolation reduces those orders to two and one. In a stiff lid-driven polar cavity, FastRK3 and standard RK3 exhibit the same order reduction: second order for $0.0625<CFL_\nu<1$ and first order below $0.0625$. The authors recommend midpoint extrapolation because the standard-approximation coefficients may be flow-dependent.

### Contributions

1. Derived FastRK3's stage-wise local error and the conditions under which its global velocity error remains third order for non-stiff flows.
2. Generalized the required Runge--Kutta coefficient condition to an arbitrary $s$-stage scheme.
3. Established the pressure-extrapolation relation and obtained $\beta=-2\alpha/3+5/6$ for the selected RK3 coefficients.
4. Distinguished endpoint, midpoint, and standard-approximation extrapolations using Taylor--Green vortices with periodic and unsteady Dirichlet boundaries.
5. Showed that FastRK3 matches standard RK3's reduced temporal order in a stiff wall-bounded cavity, with no additional penalty from intermediate pressure extrapolation.
