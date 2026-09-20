# 2026VC

## ChatGPT (July 2026)

### Summary

Entropy-correction artificial viscosity (ECAV) enforces a semi-discrete cell entropy inequality by adding only the dissipation needed to offset a local entropy residual. This paper analyzes ECAV when its viscous term is discretized by the local discontinuous Galerkin (LDG) method. Unlike the earlier BR-1 choice, whose discrete gradient has spurious nonconstant null modes, the LDG gradient admits a lower bound that yields an $O(h)$ upper bound on the elementwise viscosity coefficient. Thus ECAV does not impose an asymptotically stricter time-step condition than the hyperbolic CFL restriction. The LDG formulation retains the global entropy-dissipation estimate and, with a contact-preserving interface flux, exactly preserves representable stationary contact waves. Tests on Burgers and compressible Euler problems verify entropy stability, high-order accuracy, contact preservation, shock robustness, and minimal dissipation. In one Burgers test, LDG required 474 adaptive steps versus 20,932 for BR-1; a nodal BR-1 run stalled beyond 100,000 steps. Smooth density-wave tests also show smaller viscosity and error than a tuned modal shock-capturing method.

### Contributions

1. Recast ECAV with an LDG discretization of the entropy-dissipative viscous term.
2. Proved a lower bound for the LDG gradient and an $O(h)$ upper bound for ECAV viscosity.
3. Established that LDG ECAV satisfies the required global semi-discrete entropy inequality.
4. Proved and numerically verified preservation of stationary contact waves.
5. Demonstrated high-order accuracy, low dissipation, and substantially less time-step restriction than pathological BR-1 cases.
