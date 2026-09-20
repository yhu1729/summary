# 2026WWZ

## ChatGPT (July 2026)

### Summary

The paper constructs variable-step, second-order exponential time-differencing schemes for periodically forced incompressible Navier--Stokes equations. Its main ETD-mr-ccSAV method combines a mean-reverting scalar auxiliary variable, a concurrent second-order auxiliary-variable correction, and multistep ETD treatment of nonlinear advection. For arbitrary positive step sequences and bounded forcing, the discrete velocity or vorticity has a uniform-in-time $L^2$ bound independent of both step size and viscosity, while nonlinear advection remains explicit. Each step requires two constant-coefficient heat or Stokes solves and one scalar cubic equation. A first-order embedded companion supplies adaptive error estimates and step selection. Two-dimensional Fourier pseudospectral experiments verify second-order temporal accuracy and stable long integrations where classical ETD-MS2 and a correction-only variant can grow unstable. In Kolmogorov-flow tests, adaptive integration reproduces fixed-step mean enstrophy and flow scales while reducing computational cost; rare-event tail statistics are less accurate. Rigorous convergence and invariant-measure convergence are left open.

### Contributions

1. Combined mean-reverting and concurrent-correction SAV mechanisms with multistep ETD to obtain variable-step second-order schemes.
2. Proved uniform-in-time $L^2$ bounds under general bounded forcing for arbitrary positive step sizes and all viscosity values.
3. Reduced each update to two constant-coefficient heat or Stokes solves plus one scalar cubic equation while treating advection explicitly.
4. Built an embedded first-order companion scheme for adaptive error estimation and automatic step-size control.
5. Verified second-order accuracy, long-time robustness, statistical fidelity, and computational savings in periodic two-dimensional flow experiments.
