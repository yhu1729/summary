# 2026BCSR

## ChatGPT (July 2026)

### Summary

This paper replaces finite-difference approximations in the Cauchy--Kovalevskaya predictor of high-order Lax--Wendroff flux-reconstruction and discontinuous-Galerkin schemes with forward automatic differentiation (AD). A recursive derivative-bundle identity evaluates each temporal flux derivative as a directional derivative of the preceding one, exactly reproducing the multivariate chain rule without forming flux Jacobians or writing order-specific finite-difference formulas. The authors implement point-wise AD with Enzyme.jl and element-wise AD with TaylorDiff.jl. Because AD evaluates fluxes only at the admissible numerical state, it avoids the inadmissible perturbed states that make approximate Lax--Wendroff fail for isentropic Euler and relativistic-hydrodynamics Riemann problems. Tests recover the expected order through sixth order, preserve admissibility, and handle a Mach-2000 jet. Across Intel Xeon and Apple M3 benchmarks, AD is at least competitive with the finite-difference predictor; tested speedups reach 1.61, although whether point-wise or element-wise differentiation is faster depends on hardware. The result is a Jacobian-free, problem-independent predictor whose implementation is uniform across orders.

### Contributions

1. Derived a recursive automatic-differentiation formula for exact Cauchy--Kovalevskaya temporal flux derivatives without explicit Jacobian tensors.
2. Implemented point-wise Enzyme.jl and element-wise TaylorDiff.jl variants in Tenkai.jl and TrixiLW.jl.
3. Showed why AD avoids predictor-stage positivity corrections by never evaluating fluxes at perturbed inadmissible states.
4. Demonstrated robustness on demanding Euler and relativistic-hydrodynamics problems while recovering the expected orders through sixth order.
5. Benchmarked both AD variants on Intel and Apple CPUs, finding speedups as high as 1.61 with architecture-dependent variant rankings.
