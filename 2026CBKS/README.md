# 2026CBKS

## ChatGPT (July 2026)

### Summary

JetSCI combines JAX's automatic differentiation and GPU-vectorized local finite-element kernels with PETSc's sparse solvers, preconditioners, and MPI distribution. For heterogeneous micromechanics problems, JAX differentiates material-batched residual kernels to form dense element Jacobians, which are assembled into a sparse global operator. A GPU-resident interoperability path uses DLPack, CuPy, `ctypes`, and `petsc4py` to expose device pointers to PETSc without staging through host memory; solutions return to JAX for Newton iteration. Component-level tests compare sparse matrix--vector products, JAX and PETSc Krylov solvers, matrix-free and explicit JAX paths, direct solvers, preconditioners, and one- versus two-GPU execution. PETSc-backed paths are faster and remain convergent at sizes where several JAX or CuPy baselines fail, while two-GPU execution becomes beneficial only after communication overhead is amortized. The study is limited to a two-material benchmark and modest GPU counts; distributed matrix and vector construction is less developed than the solve phase.

### Contributions

1. Designed a hybrid differentiable-simulation architecture that assigns local differentiated kernels to JAX and global sparse solves to PETSc.
2. Built element-batched automatic Jacobian generation while preserving sparse finite-element assembly.
3. Implemented a low-copy GPU bridge through DLPack, CuPy, `ctypes`, and PETSc's native construction routines.
4. Exposed PETSc solver, preconditioner, and MPI options inside a JAX-driven Newton workflow.
5. Evaluated solver robustness, preconditioning, matrix representations, and multi-GPU crossover behavior on heterogeneous micromechanics systems.
