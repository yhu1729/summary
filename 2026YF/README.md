# 2026YF

## ChatGPT (July 2026)

### Summary

The authors combine an entropy-stable nodal discontinuous Galerkin spectral-element method for the two-dimensional compressible Euler equations with a localized oscillation-eliminating procedure on general curvilinear quadrilateral meshes. Summation-by-parts operators, discrete metric identities, and entropy-stable interface fluxes yield a semidiscrete global entropy inequality. Projection operators replace the original method's dependence on local orthogonal modal bases, while the zero-order damping coefficient becomes a troubled-cell sensor and a scale factor controls dissipation. Smooth-vortex tests on deformed meshes recover $O(h^{N+1})$ convergence and non-increasing total entropy. Shock benchmarks capture Riemann interactions, Mach-10 double reflection, Mach-3 cylinder flow, and an explosion among eight cylinders. In double-Mach reflection, localization reduces CPU time from $3123.8\,\mathrm{s}$ with all cells damped to $2570.3\,\mathrm{s}$ at threshold $0.02$ and $2128.3\,\mathrm{s}$ at $0.1$. Accuracy and dissipation depend materially on the chosen threshold and scale.

### Contributions

1. Proved semidiscrete entropy stability for DGSEM on curvilinear meshes.
2. Extended oscillation elimination to curved quadrilateral elements using projections.
3. Reused the damping coefficient as a troubled-cell indicator.
4. Demonstrated high-order convergence and entropy control on deformed meshes.
5. Quantified robustness and cost reductions on strong-shock, complex-geometry tests.
