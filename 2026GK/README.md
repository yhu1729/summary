# 2026GK

## ChatGPT (July 2026)

### Summary

This paper develops discontinuous Galerkin discretizations for the Cahn--Hilliard and coupled Cahn--Hilliard--Navier--Stokes equations with degenerate mobility. The new SIPGD-L and SWIPD-L schemes alter the penalty mobility flux using, respectively, an interface maximum and a harmonic average, providing tunable control of coercivity and stability. A coercivity result is established for the generalized mobility-dependent trilinear form. Combined with an Eyre splitting, Zhang--Shu limiter, and divergence-free velocity postprocessing, the methods are designed to retain mass conservation, energy dissipation, and phase-field bounds. Manufactured-solution studies recover optimal $L^2$ and $H^1$ convergence in two and three dimensions. Merging-droplet and rotating-droplet tests show numerical structure preservation, while $hp$-adaptivity reduces degrees of freedom and computational complexity relative to $h$-adaptivity without materially degrading accuracy. Rigorous discrete structure-preservation results for SWIPD-L beyond coercivity remain future work.

### Contributions

1. Introduced SIPGD-L and SWIPD-L with interface-maximum and harmonic-average mobility fluxes.
2. Proved coercivity of the generalized mobility-dependent DG trilinear form under an explicit penalty-flux condition.
3. Combined the schemes with Zhang--Shu limiting and $hp$-adaptive indicators while retaining numerical mass and energy structure.
4. Demonstrated optimal $L^2$ and $H^1$ convergence in two and three dimensions across four DG variants.
5. Showed that $hp$-adaptive droplet simulations preserve bounds and reduce degrees of freedom relative to $h$-adaptivity.
