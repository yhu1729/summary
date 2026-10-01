# 2026QKLM

## ChatGPT (July 2026)

### Summary

The Tempered Finite Element Method modifies standard finite elements so meshes containing nearly or exactly zero-measure elements can still converge. The motivating failure is not an isolated needle or flat cap but a band of cap elements that imposes an artificial locking constraint. TFEM clips the element-map Jacobian only where it appears in denominators, locally softening diffusion while preserving the usual formulation elsewhere. For two-dimensional Poisson problems with linear elements, the authors prove optimal convergence when the minimum Jacobian scales as $h^3$; numerical evidence gives the corresponding $h^4$ scaling in three dimensions. Exactly degenerate elements recover a nonconforming mortaring or penalty interpretation. Manufactured and randomized tests show errors close to regular-mesh finite elements, mild sensitivity to the clipping constant, and no degradation of preconditioned conjugate-gradient convergence. Numerical extensions cover elasticity, mortaring of nonconforming meshes, high-order elements, and advection. Rigorous theory is concentrated on linear Poisson elements, the optimal constant remains geometry-dependent, and general three-dimensional degeneracy criteria are unresolved.

### Contributions

1. Distinguished harmless isolated degenerate elements from locking cap-band configurations.
2. Proposed a one-line Jacobian-denominator clipping rule that defines TFEM.
3. Proved optimal convergence for the two-dimensional linear Poisson setting.
4. Established the equivalence between zero-measure TFEM and nonconforming mortaring.
5. Demonstrated robust conditioning and extensions to elasticity, high order, and advection.
