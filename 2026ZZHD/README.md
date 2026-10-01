# 2026ZZHD

## ChatGPT (September 2026)

### Summary

This paper introduces a subcell entropy-constrained (SEC) limiter for entropy-stable discontinuous Galerkin spectral element methods. Assigning different high/low-order flux blending weights to subcell interfaces improves local control of shock dissipation but can break an element's semi-discrete entropy inequality. The authors restore it by optimizing pairwise corrections to the high-order entropy-conservative flux, minimizing the corrections' deviation from unity. A two-level detector combines element modal energy with subcell oscillation measurements to choose the weights. They derive an entropy-only variant, SEC(EC), and a variant with an additional flux-consistency constraint, SEC(EC+CC). Both preserve constant states and show convergence in smooth-flow tests. In advection, shock tubes, double Mach reflection, Kelvin--Helmholtz flow, and a nonconvex scalar problem, SEC(EC) generally resolves small features more sharply than the comparison limiters while suppressing spurious oscillations. The additional consistency constraint can distort some solutions and increases runtime; the entropy-only variant is cheaper. The method addresses semi-discrete entropy stability, but the paper does not claim a general positivity guarantee.

### Contributions

1. Identified why nonuniform subcell blending weights can destroy the entropy cancellation of an entropy-stable DG scheme.
2. Derived pairwise high-order flux corrections through a constrained quadratic minimization with an explicit solution.
3. Developed entropy-only and entropy-plus-consistency limiter variants and analyzed consistency and convergence.
4. Combined element modal energy and subcell oscillation sensing to set interface-specific blending weights.
5. Compared accuracy, shock resolution, entropy behavior, and runtime against HG and Lin limiters on one- and two-dimensional problems.
