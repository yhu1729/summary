# 2026GYWG

## ChatGPT (July 2026)

### Summary

COREFL is an open-source C++/CUDA solver for high-fidelity compressible reactive-flow simulations on structured generalized curvilinear grids. It solves multicomponent compressible Navier--Stokes equations using a hybrid seventh-order WENO-Z/linear-upwind discretization, mixture-averaged transport, and balanced splitting for stiff chemical kinetics. CUDA-aware MPI supports multi-GPU execution, while static polymorphism and GPU-oriented multidimensional data structures preserve extensibility without virtual-dispatch overhead. Validation spans formal accuracy tests, inert and reactive shock tubes, oblique detonation, supersonic and hypersonic boundary layers, and a reacting turbulent mixing layer. Reported results reproduce reference shocks, heat transfer, turbulence statistics, and reacting-flow behavior. Kernel tuning reduces selected execution times by 17--35%; weak scaling remains near 90% through 16 A100 GPUs, and a reactive case shows more than 800-fold speedup over one core of an in-house CPU solver. Deployment currently depends on NVIDIA CUDA and CUDA-aware MPI.

### Contributions

1. Released an Apache-2.0 C++/CUDA/MPI solver for compressible multicomponent reactive-flow direct and large-eddy simulations.
2. Integrated hybrid seventh-order WENO-Z/upwind convection, detailed mixture transport, and balanced chemical-kinetics splitting.
3. Used compile-time polymorphism to extend physical models with little runtime overhead or code duplication.
4. Designed and profiled GPU-specific data layouts and kernels, obtaining 17--35% reductions in selected kernel times.
5. Demonstrated broad physical validation, near-90% weak-scaling efficiency through 16 GPUs, and over 800-fold reactive-case acceleration relative to a CPU core.
