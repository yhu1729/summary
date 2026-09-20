# 2026CKLS

## ChatGPT (July 2026)

### Summary

This work extends the parallel basis-update-and-Galerkin integrator for dynamical low-rank matrix equations to Tucker tensors and general tree tensor networks. During each time step, differential equations for all leaf bases and connecting tensors are evolved concurrently; only hierarchical orthogonalization remains sequential. The method adapts tensor ranks, avoids backward time integration, and omits the augmented-rank connecting-tensor update required by an earlier rank-adaptive scheme. The authors prove a first-order global error bound whose constants are independent of small singular values, establishing robustness in regimes where conventional integrators become restrictive. Tests on long-range quantum spin dynamics and uncertain radiative-transfer benchmarks reproduce the predicted first-order behavior and agree with reference solutions. Even in serial implementations, removing augmented-rank coefficient updates reduces runtimes, including from 30 to 12 seconds for the plane-source case and from 105 to 72 seconds for the line-source case. The additional speedup available from genuinely parallel execution remains hardware-dependent and was not measured.

### Contributions

1. Extended a robust parallel low-rank matrix integrator to Tucker tensors and arbitrary tree tensor networks.
2. Enabled concurrent evolution of every basis and connecting tensor within a time step.
3. Established a first-order error bound independent of small matricization singular values.
4. Combined rank adaptivity with forward-only evolution and avoided augmented-rank connecting-tensor updates.
5. Demonstrated accuracy and serial runtime reductions on quantum and uncertain radiative-transfer problems.
