# 2026MRG

## ChatGPT (July 2026)

### Summary

The paper constructs arbitrary-order discontinuous spectral-element schemes for rotating shallow-water equations with variable topography on curved manifolds. A covariant balance-law formulation, skew-symmetric tensor-divergence split, tensor-product summation-by-parts operators, and flux differencing yield methods that are well balanced, mass conservative, and either total-energy conservative or dissipative according to the interface flux. Analytic geometry and metric terms can be used directly, avoiding approximate metric identities normally required for entropy proofs. The authors prove conservation, entropy stability, and lake-at-rest well balancing on general unstructured quadrilateral grids. Cubed-sphere experiments involving unsteady solid-body rotation, isolated-mountain flow, barotropic instability, and Rossby-Haurwitz waves verify optimal order $p+1$, machine-level conservation for entropy-conservative fluxes, controlled energy dissipation for entropy-stable fluxes, and robustness for under-resolved vortical flows and long integrations. The formulation is positioned as a foundation for a three-dimensional atmospheric dynamical core.

### Contributions

1. Developed a split, flux-differencing covariant shallow-water DG spectral-element formulation on curved manifolds.
2. Derived entropy-conservative and entropy-stable two-point and interface fluxes.
3. Proved mass conservation, energy conservation or dissipation, and lake-at-rest well balancing on curved quadrilateral meshes.
4. Avoided enforced discrete metric identities through analytical geometry representation.
5. Verified optimal convergence and long-time robustness across four cubed-sphere atmospheric benchmarks.
