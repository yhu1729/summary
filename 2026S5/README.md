# 2026S5

## ChatGPT (July 2026)

### Summary

FastLSQ represents solutions with frozen sinusoidal random Fourier features whose derivatives of any order have closed forms. This permits graph-free assembly of differential operators: linear PDEs require one least-squares solve, while nonlinear PDEs use Newton--Raphson iterations that reuse analytical assembly. Across 17 PDE benchmarks spanning one to six dimensions, the method attains relative $L^2$ errors near $10^{-7}$ within $0.1\,\mathrm{s}$ for linear problems and $10^{-8}$--$10^{-9}$ within $9\,\mathrm{s}$ for five nonlinear solver problems on a single NVIDIA T4. Controlled comparisons attribute substantial accuracy gains over a one-shot $\tanh$ basis to the sinusoidal features. Exact derivatives also support noisy PDE discovery, inverse heat-source localization, and sparse-sensor coil recovery. Current limitations include problem-specific bandwidth selection, conditioning growth for high derivatives, penalty tuning, and a focus on box domains.

### Contributions

1. Derived an operator-agnostic closed-form formula for arbitrary-order derivatives of sinusoidal random features.
2. Reduced linear PDE solution to one analytical least-squares assembly and solve without automatic differentiation.
3. Extended the framework to nonlinear PDEs through regularized, warm-started Newton iterations with line search and continuation.
4. Benchmarked value, gradient, residual, runtime, and ablation behavior on 17 linear and nonlinear PDEs.
5. Demonstrated differentiable inverse problems and substantially cleaner derivative estimation for sparse-regression PDE discovery.
