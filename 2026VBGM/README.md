# 2026VBGM

## ChatGPT (July 2026)

### Summary

This work develops backward semi-Lagrangian advection for Vlasov-type equations on multi-patch meshes using local cubic B-splines. Merely enforcing $C^0$ continuity at patch interfaces can be unstable, so the method imposes Hermite conditions with $C^1$ continuity and reconstructs interface derivatives. A generalized derivative formula handles uniform or nonuniform cells, conforming interfaces, selected nonconforming interfaces, and T-joints. In the conforming case, solving a small global system makes the local splines coincide with the corresponding global spline and can recover $C^2$ continuity. A cheaper localized approximation is also derived: distant data have decreasing influence, and about 30 cells per patch reach machine precision in the tested uniform configurations. Implemented in Gyselalib++, the method reproduces global-spline interpolation, fourth-order convergence when sufficiently many cells enter the derivative approximation, and two-dimensional guiding-center advection through patch interfaces. Nonconforming refinement achieves accuracy comparable to a refined global mesh with fewer cells. Tests include O-point and T-joint geometries; treating the X-point needed for a complete tokamak cross-section remains future work.

### Contributions

1. Established that $C^0$ patch coupling can be unstable and adopted $C^1$ Hermite coupling.
2. Generalized interface-derivative reconstruction to nonuniform, conforming, and selected nonconforming meshes.
3. Recovered the equivalent global cubic spline through a small interface system in conforming cases.
4. Derived controllably local approximations whose distant-point influence decays with patch size.
5. Validated the method in Gyselalib++ on O-point, nonconforming, and T-joint guiding-center problems.
