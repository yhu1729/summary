# 2026LV

## ChatGPT (July 2026)

### Summary

Parabolic optimal-control discretizations produce coupled forward--backward systems that cannot be advanced by ordinary sequential time stepping and become expensive at scale. This paper studies a time-parallel Schwarz domain-decomposition method and asks whether convergence remains effective as the number of fixed-size time subintervals grows. Two complementary analyses characterize the iteration matrix. A problem-tailored matrix norm gives a spectral-radius bound strictly below one and independent of the subinterval count. Block Toeplitz theory then locates every eigenvalue nonasymptotically within the same bound and characterizes the limiting spectrum as the count tends to infinity. Together these results establish weak scalability under the paper's assumptions. Scalar-mode, heat-control, and periodic advection--diffusion experiments show that the bounds are sharp and iteration counts remain essentially independent of the interval count, including a discretization with more than eight million state-and-adjoint unknowns. The analysis provides a basis for future multilevel methods and high-performance implementations, which are not developed here.

### Contributions

1. Formulated a weak-scalability analysis for time-parallel Schwarz iteration on parabolic optimal-control systems.
2. Constructed a tailored matrix norm yielding an interval-count-independent spectral-radius bound below one.
3. Used block Toeplitz theory to locate all eigenvalues nonasymptotically in the complex plane.
4. Characterized the asymptotic convergence spectrum as the number of time subintervals grows.
5. Confirmed numerically that the estimates sharply predict the observed convergence behavior.
