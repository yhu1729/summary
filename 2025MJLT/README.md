# 2025MJLT

## ChatGPT (July 2026)

### Summary

JAX-in-Cell is a fully electromagnetic, multispecies, relativistic 1D3V particle-in-cell framework implemented entirely in JAX. The code is designed as a bridge between compact educational PIC scripts and larger production frameworks, using just-in-time compilation and automatic vectorization to run efficiently on CPUs, GPUs, and TPUs. It solves the Vlasov--Maxwell system on a staggered Yee lattice with periodic, reflective, or absorbing boundary conditions. Particle motion can be advanced with an explicit Boris pusher or with an implicit Crank--Nicolson method solved by Picard iteration for improved energy behavior. Because the implementation is differentiable end to end, it supports gradient-based optimization and integration with AI workflows. The paper documents the numerical methods, validates the framework against standard plasma benchmarks, and demonstrates automatic-differentiation capabilities. Its main significance is to make PIC modeling more accessible for differentiable physics while retaining electromagnetic, relativistic, multispecies functionality in a modern Python-based software stack.

### Contributions

1. Introduced a JAX-based 1D3V electromagnetic PIC framework for relativistic, multispecies plasma simulations.
2. Implemented the Vlasov--Maxwell system on a staggered Yee lattice with multiple boundary-condition options.
3. Provided both explicit Boris and implicit Crank--Nicolson particle advance options.
4. Used JIT compilation and vectorization to target CPU, GPU, and TPU execution from Python.
5. Demonstrated differentiable PIC simulations suitable for gradient-based optimization and AI-assisted plasma modeling.
