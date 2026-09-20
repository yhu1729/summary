# 2025VR

## ChatGPT (July 2026)

### Summary

This paper develops two high-order methods for integrating functions known on scattered surface point clouds without triangulation, prescribed point layouts, or closed-form basis-function moments. Both methods use norm-minimizing Hermite--Birkhoff interpolation and inherit its super-algebraic convergence. Method 1 determines the scaling that makes a Poisson problem solvable and thereby computes ratios of integrals, including surface averages; it applies directly to closed surfaces and surfaces with boundary. Method 2 uses the divergence theorem to reduce a surface integral to boundary line integrals without imposing boundary conditions. It evaluates integrals and surface areas directly, but closed surfaces must first be partitioned into patches with boundary. Numerical tests on irregular point distributions and a genus-two surface show substantially higher accuracy than Monte Carlo or linear triangulation. The framework is also augmented with known singular functions, retaining rapid convergence for logarithmic and inverse-distance singular integrands without refining the point cloud near the singularity.

### Contributions

1. Developed two fully meshfree high-order quadrature methods for arbitrary piecewise-smooth surfaces.
2. Formulated a Poisson-solvability method for ratios of surface integrals and average values.
3. Derived a divergence-theorem method for direct integrals and accurate surface-area estimation.
4. Preserved super-algebraic convergence for scattered, nonuniform point clouds without triangulation.
5. Extended norm-minimizing interpolation to singular integrands without local point refinement.
