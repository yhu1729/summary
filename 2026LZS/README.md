# 2026LZS

## Codex/ChatGPT (September 2026)

### Summary

A recursive Jacobian-free Cauchy–Kovalevskaya procedure simplifies high-order compact central schemes for hyperbolic conservation laws. The Cauchy–Kovalevskaya procedure obtains time derivatives from the governing equations; here, local Taylor polynomials supply virtual-point flux values, and repeated central differences replace analytical flux-derivative tensors. A uniform recursion accommodates arbitrary derivative orders without enlarging the underlying computational-cell stencil. The analysis establishes second-order virtual-step errors and exact equivalence to the analytical procedure for constant-coefficient linear systems, preserving their linear stability restrictions. Virtual steps balance differencing errors against roundoff. A total-variation-bounded troubled-cell detector replaces the earlier nonlinear limiter; flagged cells retain their averages but receive limited slopes and lose higher derivatives. Burgers and one- and two-dimensional Euler tests demonstrate second- through seventh-order convergence before numerical-error saturation, together with shock and small-vortex resolution. Higher order improves accuracy per computational cost in the reported smooth test, although the fourth-order recursive method is slower than its nonrecursive Jacobian-free predecessor. Demonstrated accuracy is limited to seventh order; still higher orders face increasing virtual-difference errors, and the Euler limiter parameter is chosen empirically.

### Contributions

1. Constructed a single recursive formula for mixed space-time flux derivatives using locally reconstructed virtual points, eliminating order-specific symbolic derivative tensors and differencing formulas.
2. Proved the virtual-step error estimate, including propagated Taylor-reconstruction errors, and equivalence to exact Cauchy–Kovalevskaya differentiation for constant-coefficient linear fluxes.
3. Derived derivative-order-dependent virtual-step choices that balance roundoff amplification and differencing error, with an additional cap from physical mesh and time steps.
4. Adapted troubled-cell detection and characteristic slope limiting to compact central schemes, retaining conservative cell averages and enabling shock calculations through seventh order.
5. Verified convergence with smooth Burgers and Euler solutions and assessed shock capturing with shock tubes, blast waves, shock–entropy interaction, double Mach reflection, and multidimensional Riemann problems.
