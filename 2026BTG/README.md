# 2026BTG

## ChatGPT (July 2026)

### Summary

The paper develops a von Neumann stability analysis for explicit and implicit arbitrary-Lagrangian--Eulerian ADER discontinuous Galerkin schemes for hyperbolic equations. On classical one-dimensional spacetime meshes, it derives amplification-matrix criteria, clarifies the limited validity of commonly used CFL values at higher polynomial degrees, and bounds admissible mesh velocities. It then models topology-changing moving meshes by inserting degenerate sliver spacetime elements that have zero spatial size at time-step endpoints but nonzero spacetime volume. Conservative predictor and corrector formulations exchange fluxes through these slivers without projection or reconstruction. The analysis and numerical studies show that slivers do not alter the explicit scheme's classical CFL restrictions. The implicit scheme is stable throughout the tested parameter range, with a proof for a representative sliver configuration. Linear-advection convergence tests recover the expected consistency order for both formulations. The analysis is restricted to scalar one-dimensional model problems, so nonlinear systems and multidimensional topology changes remain future work.

### Contributions

1. Formulated explicit and implicit direct ALE ADER-DG schemes in a common spacetime framework.
2. Derived Fourier amplification-matrix stability criteria for the explicit method.
3. Showed that conventional higher-order CFL values can be weakly unstable and derived mesh-velocity restrictions.
4. Extended conservative predictor and corrector formulations to degenerate sliver elements representing mesh topology changes.
5. Established unchanged explicit CFL behavior with slivers, proved an implicit stability case, and verified the expected consistency orders.
