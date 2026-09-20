# 2026RARB

## ChatGPT (July 2026)

### Summary

This paper documents major SUNDIALS capabilities introduced from versions 6.2.0 through 7.4.0. ARKODE gains low-storage Runge--Kutta methods, including strong-stability-preserving and super-time-stepping families; symplectic partitioned Runge--Kutta methods up to order ten; and flexible standard and forcing-based operator splitting through a common `SUNStepper` interface. Multirate methods now adapt slow and fast time scales, while explicit Runge--Kutta methods support discrete adjoint sensitivity analysis with checkpointing. KINSOL adds runtime control of Anderson-acceleration damping and depth, and library-wide logging and error handling become more uniform. The implementations reuse SUNDIALS abstractions for shared-memory, distributed-memory, and GPU data. Gray--Scott experiments recover splitting orders through six and show more than an order-of-magnitude RKC speedup over a conventional second-order explicit method at loose tolerances. Lotka--Volterra tests recover the expected third- through fifth-order convergence for forward states and adjoint gradients.

### Contributions

1. Added low-storage SSP and super-time-stepping Runge--Kutta integrators for memory-constrained and diffusion-dominated simulations.
2. Added high-order symplectic partitioned Runge--Kutta methods for separable Hamiltonian systems.
3. Introduced flexible operator-splitting modules and a common interface for composing SUNDIALS, custom, or exact subintegrators.
4. Extended multirate temporal adaptivity and explicit Runge--Kutta discrete adjoint sensitivity analysis.
5. Improved Anderson acceleration, error handling, and logging and validated representative convergence and performance behavior.
