# 2024BC

## ChatGPT (July 2026)

### Summary

This paper analyzes implicit--explicit Runge--Kutta discretizations of the ellipsoidal-statistical BGK kinetic model in the small-Knudsen-number regime. Through a discrete Chapman--Enskog expansion, the authors extend Navier--Stokes-level asymptotic analysis from a special class of schemes to general Type I and Type II IMEX-RK methods. They derive conditions under which the numerical distribution and its moments approximate the compressible Navier--Stokes limit without resolving collision times proportional to the Knudsen number. The analysis also identifies order-reduction mechanisms and additional stage-order and coupling conditions needed for uniform accuracy across kinetic and fluid regimes. Among examined methods, a Type II, asymptotically accurate IMEX-II-ISA3 construction satisfies the extra conditions and avoids the observed Navier--Stokes-level order loss. Relaxation, smooth-flow, and shock-tube experiments support the truncation-error results and show agreement of stress and heat flux with their Navier--Stokes closures. The guarantees depend on well-prepared data and the stated regularity and coefficient conditions; arbitrary IMEX schemes do not automatically retain their nominal order in the fluid limit.

### Contributions

1. Extended Navier--Stokes asymptotic analysis to general Type I and Type II IMEX-RK schemes.
2. Derived discrete Chapman--Enskog expansions and local truncation errors for the ES-BGK model.
3. Identified algebraic conditions controlling asymptotic accuracy and fluid-limit order reduction.
4. Highlighted an IMEX-II-ISA3 scheme that maintains uniform accuracy under those conditions.
5. Verified the theory with relaxation, smooth-flow, and shock-tube numerical experiments.
