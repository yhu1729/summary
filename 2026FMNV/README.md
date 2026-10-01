# 2026FMNV

## ChatGPT (July 2026)

### Summary

Grid-based solvers for advection--diffusion equations suffer exponential growth in cost with dimension, while explicit Eulerian methods also face stability-limited timesteps. The proposed neural semi-Lagrangian method represents the spatial and parametric solution with a neural network and advances it sequentially in time. After fitting the initial condition, each step traces backward characteristics and optimizes a new network to match the transported previous solution; stochastic characteristic sampling extends the construction to diffusion. The method is mesh-free, highly parallel on GPUs, and has no timestep restriction for stability. Rough estimates separate characteristic-integration, neural approximation, optimization, and sampling errors, and the implementation adds natural-gradient preconditioning, adaptive sampling, and boundary treatments. Tests cover parametric transport, Vlasov dynamics, two- and three-dimensional level-set deformation, advection--diffusion through eight dimensions, and a Vlasov--Poisson proof of concept. Compared with PINNs, neural Galerkin methods, and classical semi-Lagrangian schemes, it maintains competitive accuracy at lower cost and becomes increasingly advantageous in high dimensions. Its main weakness is repeated nonconvex optimization: training becomes harder during long-time, fine-structure evolution, and the available analysis gives only rough rather than rigorous convergence guarantees.

### Contributions

1. Replaced grid interpolation in semi-Lagrangian time stepping with projection onto a neural-network approximation space.
2. Extended the mesh-free construction from advection to diffusion through stochastic backward characteristics.
3. Derived an error decomposition covering characteristic, approximation, optimization, and sampling errors.
4. Demonstrated GPU-parallel solutions for parametric, kinetic, level-set, and eight-dimensional advection--diffusion problems.
5. Showed favorable high-dimensional accuracy and cost against PINN, neural Galerkin, and classical semi-Lagrangian baselines.
