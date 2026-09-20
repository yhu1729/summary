# 2026LMSH

## ChatGPT (July 2026)

### Summary

The authors extend TRIMEG-C1 with a high-order, $C^1$-continuous, piecewise field-aligned finite-element method for global electromagnetic gyrokinetic particle-in-cell simulations spanning tokamak core, separatrix, and open-field-line regions. Locally field-aligned basis functions combine with unstructured triangular poloidal meshes in cylindrical coordinates, preserving parallel accuracy without the distortion and separatrix singularity of globally field-aligned coordinates. The formulation supports $\delta f$ and full-$f$ models and couples mixed-variable electromagnetic equations, generalized pullback mitigation of cancellation, and an iterative Ampère solver with analytically controlled skin-depth terms. Linear simulations of TCV-X21 reproduce expected electromagnetic ion-temperature-gradient and kinetic-ballooning-mode behavior. Scans over toroidal mode number, plasma $\beta$, and normalized machine size capture the ITG-to-KBM transition and shifts in dominant modes. Multi-mode nonlinear runs demonstrate three-dimensional electromagnetic capability without toroidal filtering.

### Contributions

1. Extended piecewise field-aligned finite elements to whole-volume tokamak geometry with open field lines.
2. Combined high-order $C^1$ triangular elements with local field alignment to avoid global-coordinate singularities.
3. Integrated mixed-variable and generalized pullback schemes for electromagnetic cancellation control.
4. Validated ion-temperature-gradient and kinetic-ballooning physics through TCV-X21 parameter scans.
5. Demonstrated multi-mode three-dimensional electromagnetic gyrokinetic particle simulations without toroidal filtering.
