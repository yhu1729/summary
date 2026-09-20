# 2025RAML

## ChatGPT (July 2026)

### Summary

This paper develops adaptive step-size control for embedded multirate infinitesimal (MRI) integrators. Its Decoupled controllers independently regulate slow and fast errors without estimating accumulated fast error, while H-Tol controllers allocate a requested tolerance between the scales using such an estimate. Both outperform the earlier H-h family on the tested three-scale KPR and stiff Brusselator problems, where H-h often fails to maintain adequate scale separation. H-Tol performs best when slow evaluations dominate cost; Decoupled is preferable when slow and fast costs are comparable. The framework theoretically supports arbitrarily many time scales, although experiments use three. The paper also constructs embeddings for explicit multirate exponential Runge--Kutta methods of orders two through five, including the first fifth-order embedded MRI method, and compares explicit, implicit, and implicit--explicit MRI schemes. Results emphasize that method, controller, and right-hand-side splitting choices remain problem-dependent; large-scale PDE applications are future work.

### Contributions

1. Introduced Decoupled multirate controllers that regulate slow and fast errors independently.
2. Developed H-Tol controllers that distribute tolerance using accumulated fast-error estimates.
3. Established a controller design that theoretically extends to an arbitrary number of time scales.
4. Constructed embedded multirate exponential Runge--Kutta formulas of orders two through five, including the first fifth-order embedded MRI scheme.
5. Compared a broad set of embedded MRI methods and controllers and identified cost-dependent selection trade-offs.
