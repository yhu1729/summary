# 2026HLLS

## ChatGPT (July 2026)

### Summary

This paper develops an adaptive variational physics-informed neural network (VPINN) method for stationary Navier-Stokes equations. Its a posteriori estimator combines projection errors in the PDE terms, data oscillation, VPINN loss, and element and interelement residuals. Under regularity and proximity assumptions, the authors prove that the estimator bounds the velocity $H^1$ and pressure $L^2$ error from above and is locally efficient up to projection and data-oscillation terms. Two-dimensional tests use Kovasznay flow and a singular solution on an L-shaped domain. The estimator tracks the true error, identifies steep-gradient and singular regions, and drives Dörfler mesh refinement. With comparable quadrature-point counts, adaptive meshes produce smaller errors and estimator values than uniform refinement. On very fine meshes the estimator can stagnate, which the authors associate with mesh-dependent local efficiency and difficulty optimizing the nonconvex VPINN loss.

### Contributions

1. Constructed a locally computable four-part a posteriori estimator for stationary Navier-Stokes VPINNs.
2. Proved global reliability for the combined velocity $H^1$ and pressure $L^2$ error near a regular solution.
3. Established local efficiency estimates for volume residuals, divergence defects, flux jumps, and VPINN loss.
4. Integrated the estimator with Dörfler marking to adapt the VPINN test-space mesh.
5. Demonstrated improved accuracy over uniform refinement for steep-gradient and singular benchmark solutions.
