# 2026P

## ChatGPT (July 2026)

### Summary

Many hyperbolic systems implicitly preserve the curl or divergence of a vector field, but ordinary discretizations can destroy these differential constraints. This paper proves that a classical, fully discontinuous and collocated discontinuous Galerkin (DG) method can preserve them exactly when it uses vector approximation spaces compatible with a discrete de Rham complex and a suitably directed numerical-flux diffusion. Curl preservation requires diffusion parallel to face normals, whereas divergence preservation requires orthogonal diffusion. The conserved discrete quantities are defined through adjoint curl and divergence operators, which fit naturally into the weak Galerkin formulation. The framework also provides potential-based initialization of constraint-satisfying fields and, for the induction equation, a discrete transport equation for the adjoint divergence. Tests on two-dimensional Maxwell, wave, and induction systems over Cartesian, triangular, and quadrilateral meshes confirm machine-precision constraint preservation and high-order accuracy. The experiments cover linear systems; extending stable, limited schemes to nonlinear problems remains open.

### Contributions

1. Proved exact DG preservation of adjoint curl and divergence constraints under explicit space-and-flux conditions.
2. Connected the required vector approximation spaces and discrete operators through a de Rham framework.
3. Identified the numerical-flux diffusion directions needed for curl and divergence preservation.
4. Derived constraint-compatible initialization and an adjoint-divergence transport equation for induction.
5. Verified sharpness, high-order accuracy, and machine-precision preservation on three linear hyperbolic systems.
