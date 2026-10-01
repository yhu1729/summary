# 2026P2

## ChatGPT (September 2026)

### Summary

Pavlov presents moljax, an open-source JAX method-of-lines library for stiff reaction--diffusion equations on structured grids. It combines GPU-compiled adaptive stepping, matrix-free Newton--Krylov solves with automatic-differentiation Jacobian--vector products, and Fourier-based operators and preconditioners for constant-coefficient diffusion. Its integrators include explicit Runge--Kutta, Crank--Nicolson, implicit--explicit splitting, and exponential time differencing. Controlled benchmarks on Gray--Scott, Schnakenberg, and Brusselator systems find the splitting and exponential methods 10--17 times faster than explicit RK4 on the same GPU and spatial discretization; only ETDRK4 shows monotone pointwise convergence in the reported pattern-forming tests. The FFT preconditioner reduces GMRES iterations by as much as 509-fold in diffusion-dominated cases. A tubular-reactor comparison reports an 18--40-fold speedup over Diffrax for the tested settings. FFT diagonalization assumes constant diffusion on structured grids, and initial compilation adds overhead.

### Contributions

1. Implemented JIT-compatible adaptive step acceptance and rejection on GPU using JAX control flow.
2. Built matrix-free Newton--Krylov solvers with automatic-differentiation Jacobian--vector products.
3. Used FFT, sine, and cosine transforms for diffusion solves and physics-based preconditioning.
4. Compared explicit, implicit, splitting, and exponential integrators under matched benchmark conditions.
5. Released software and reproduction scripts with performance decompositions and a reactor sensitivity example.
