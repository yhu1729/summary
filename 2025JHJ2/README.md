# 2025JHJ2

## ChatGPT (July 2026)

### Summary

This paper presents a conservative discontinuous Galerkin method for kinetic equations posed on smooth manifolds. Particle motion is represented through both canonical and non-canonical Hamiltonian formulations, with the canonical version giving a particularly efficient update while exactly conserving particle density and energy. The collisionless transport step is coupled to a BGK relaxation operator. Because BGK collisions must preserve density, momentum, and energy, the authors construct an iterative correction so the discrete collision update respects those invariants. Rotating manifolds are incorporated by modifying the Hamiltonian without abandoning the canonical structure. Test cases include manifold kinetic analogues of the Sod shock, Kelvin--Helmholtz instability on spherical and paraboloidal surfaces, and rotating variants. The paper closes by positioning the method as a route toward kinetic simulations in general relativity, where manifold geometry is intrinsic rather than a coordinate artifact.

### Contributions

1. Developed a conservative DG algorithm for kinetic equations on smooth manifolds.
2. Compared canonical and non-canonical Hamiltonian formulations for particle motion.
3. Coupled collisionless manifold transport to a BGK collision operator.
4. Added an iterative BGK correction that preserves collisional invariants numerically.
5. Validated the method on shock, instability, and rotating-manifold kinetic tests.
