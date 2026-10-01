# 2026WWQW

## ChatGPT (July 2026)

### Summary

2DESR directly solves the two-dimensional gyrokinetic eigenvalue problem for electrostatic ion-temperature-gradient modes in tokamaks. Starting from the linear Vlasov--Poisson system with adiabatic electrons, the formulation retains passing and trapped ions, finite-Larmor-radius effects, and coupled poloidal harmonics in Fourier coordinates $(z,m)$ with $z=nq(r)-m$. Finite differences in $z$ and parallel velocity, Gauss--Laguerre quadrature in magnetic moment, multipoint gyro-averaging, PARDISO linear solves, and a Newton eigenvalue iteration produce eigenfrequencies and global mode structures. Cyclone-case scans over toroidal mode number agree with GENE and NLT eigenvalues and with NLT eigenfunctions at both low and high $n$. Unlike initial-value solvers, 2DESR resolves two simultaneously unstable ITG branches, with different radial localization and growth-rate peaks near $n=20$ and $n=30$. The branch competition explains a prior GENE--GKW frequency mismatch and the unusually long time evolution required near $n=35$.

### Contributions

1. Derived a two-dimensional poloidal-Fourier gyrokinetic eigenproblem retaining full ion kinetics and coupled radial and poloidal structure.
2. Implemented finite-difference, Gauss--Laguerre, gyro-average, sparse-linear-solve, and Newton components in the 2DESR code.
3. Used $(z,m)$ position coordinates and $(v_\parallel,\mu)$ velocity coordinates to treat passing and trapped ions uniformly with manageable cost.
4. Benchmarked eigenvalues and global eigenmode structures against the GENE and NLT initial-value codes for low- and high-$n$ Cyclone cases.
5. Identified two coexisting ITG branches with distinct radial localization and explained an earlier inter-code real-frequency discrepancy.
