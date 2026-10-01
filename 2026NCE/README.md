# 2026NCE

## ChatGPT (September 2026)

### Summary

This paper extends the Reduced Augmentation Implicit Low-rank (RAIL) integrator from matrix-valued problems to three-dimensional convection--diffusion equations represented by Tucker tensors. Spectral spatial discretization and implicit--explicit Runge--Kutta time stepping first produce fully discrete tensor equations. At every Runge--Kutta stage, bases from earlier stages are augmented, compressed, and updated dimension by dimension; a Galerkin solve then advances the Tucker core. This construction permits rank adaptation and high-order time accuracy while treating diffusion implicitly and retaining low-rank storage. A postprocessing step truncates the tensor without sacrificing prescribed mass, momentum, and energy moments. Analysis distinguishes three-dimensional RAIL from Tucker Basis Update and Galerkin methods, whose inactive modes effectively remain frozen. Tests on linear convection--diffusion, Fokker--Planck dynamics, and viscous Burgers equations recover the designed temporal orders, track evolving ranks, and preserve the targeted moments. The richer augmented spaces improve robustness and accuracy but can cost substantially more per step than Tucker-BUG at higher Runge--Kutta order.

### Contributions

1. Extended RAIL integration to third-order Tucker tensors for three-dimensional convection--diffusion equations.
2. Combined rank adaptation with high-order IMEX Runge--Kutta schemes through reduced stage-basis augmentation.
3. Developed dimension-by-dimension basis updates followed by a Galerkin core solve.
4. Preserved mass, momentum, and energy during low-rank truncation through conservative postprocessing.
5. Demonstrated designed accuracy and robustness on convection--diffusion, Fokker--Planck, and viscous Burgers tests.
