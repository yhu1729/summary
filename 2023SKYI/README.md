# 2023SKYI

## ChatGPT (July 2026)

### Summary

This work connects Boost Odeint to OpenFPM by defining custom distributed state types, an algebra for elementwise operations and global norms, and CUDA/HIP operations for GPU backends. Odeint's explicit multistage, multistep, symplectic, and adaptive steppers can thereby act on OpenFPM vectors while MPI halo exchange and spatial discretization remain inside a reusable system functor. The separation lets users change time-stepping schemes independently of the right-hand side, spatial method, and target architecture, while retaining OpenFPM's expression language. Accuracy tests for exponential and sigmoidal dynamics recover expected orders through eighth order and give identical results across process counts. A three-dimensional Gray--Scott reaction--diffusion benchmark attains about 80% strong-scaling efficiency through 512 CPU cores; adaptive Dormand--Prince stepping roughly halves runtime without a significant scalability penalty. In a smoothed-particle-hydrodynamics dam-break case, the interface adds at most 6.6% CPU overhead, adds no significant GPU overhead, and runs about five times faster on one RTX 4090 than on 32 CPU cores without handwritten CUDA. A 60-line Gray--Scott example illustrates compactness. Current limitations include explicit methods only, state dimension at most six, and no support for stiff or implicit Odeint integrators.

### Contributions

1. Implemented interoperable OpenFPM state types and distributed Odeint algebras for MPI-parallel CPU execution.
2. Added CUDA and HIP operation backends so the same time-integration interface targets single- and multi-GPU systems.
3. Separated temporal integration from model right-hand sides, spatial operators, communication, and hardware through template expressions and system functors.
4. Verified the designed convergence orders of fixed-step, adaptive, and multistep schemes independently of process count.
5. Demonstrated low interface overhead, 80% strong-scaling efficiency on 512 CPU cores, and approximately fivefold GPU speedup in representative PDE and particle simulations.
