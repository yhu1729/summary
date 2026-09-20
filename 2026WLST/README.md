# 2026WLST

## ChatGPT (September 2026)

### Summary

This paper develops an efficient compatible finite-element solver for the stiff magnetic-wave subsystem of low-$\beta$ resistive magnetohydrodynamics in realistic three-dimensional tokamak geometry. An implicit--implicit time split separates fast Alfv\'en waves and anisotropic heat transport from slower acoustic dynamics while retaining the required coupling. A curl-conforming magnetic-field discretization preserves a discrete divergence constraint. The authors design a matching velocity space so that the Lorentz-force coupling retains an anisotropic curl--curl structure after block elimination. A physics-based block preconditioner then forms a magnetic-field Schur complement and applies auxiliary-space Maxwell multigrid to its dominant operator. Spatial-convergence tests confirm the intended accuracy and discrete energy behavior. Refinement studies on an ITER-like configuration show moderate robustness on anisotropic meshes and demonstrate that the tailored velocity space is necessary to keep iteration counts low at larger timesteps and finer resolutions. Longer nonlinear runs for near-equilibrium, resistive-decay, and kink-instability scenarios produce the expected field evolution with practical iteration counts and runtimes, establishing a scalable route beyond geometry-specific direct solvers.

### Contributions

1. Combined constrained-transport finite elements with an implicit--implicit split tailored to stiff tokamak MHD dynamics.
2. Designed a velocity space that preserves the Lorentz-induced curl--curl structure in the magnetic Schur complement.
3. Constructed a physics-based block preconditioner using auxiliary-space Maxwell multigrid.
4. Verified spatial accuracy, discrete magnetic divergence preservation, and consistent energy behavior.
5. Demonstrated robust nonlinear performance on anisotropic three-dimensional tokamak tests, including a kink instability.
