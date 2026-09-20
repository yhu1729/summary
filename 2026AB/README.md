# 2026AB

## ChatGPT (July 2026)

### Summary

The paper develops locally and globally conservative discontinuous Galerkin tracer transport for compatible finite-element dynamical cores. Rather than advecting a mixing ratio $m$, it advances tracer density $\rho m$ alongside dry density $\rho$ after mapping both fields into a shared discontinuous transport space. Conservative Galerkin projection, recovery, and injection preserve tracer mass when $m$ is either co-located with or vertically staggered from $\rho$ on a Charney--Phillips grid. Recovered-space transport provides second-order accuracy for lowest-order elements, while embedded DG handles vertically continuous thermodynamic spaces. A consistency correction preserves spatially constant mixing ratios. A mean-mixing-ratio limiter blends the higher-order field with a mass-equivalent lowest-order projection to enforce non-negativity for co-located spaces. Gusto tests on spherical and vertical-slice transport, terminator toy chemistry, and a moist rising bubble show near-machine-precision mass conservation without degrading convergence, whereas advective-form controls accumulate larger mass errors. Extending the limiter to vertically staggered spaces and enforcing full monotonicity remain future work.

### Contributions

1. Formulated DG transport for tracer density $\rho m$, giving conservative evolution of dry density and tracer mass.
2. Defined conservative and consistent projection, recovery, and injection operators for density and mixing ratios in different spaces.
3. Combined recovered-space and embedded-DG mappings for co-located and vertically staggered tracer configurations.
4. Developed a mean-mixing-ratio limiter that preserves cell tracer mass while enforcing non-negativity for co-located spaces.
5. Validated conservation, consistency, accuracy, chemistry coupling, and moist dynamical-core behavior in Gusto tests.
