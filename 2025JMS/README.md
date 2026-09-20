# 2025JMS

## ChatGPT (July 2026)

### Summary

Block-tridiagonal symmetric positive-definite systems appear repeatedly in state estimation and optimal control, where solution latency can limit real-time operation. The BlockDSS implementation applies recursive Schur-complement reduction, eliminating alternating block rows and producing a hierarchy of smaller independent systems. At each level, factorization and triangular-solve work is expressed with batched BLAS and LAPACK kernels, exposing GPU parallelism while preserving the known block structure. A common implementation targets both NVIDIA and AMD devices. Benchmarks show substantial acceleration over CPU sparse-direct solvers CHOLMOD and HSL MA57 and performance competitive with NVIDIA cuDSS for favorable block sizes. The study also identifies two practical limits: recursion levels still launch batched operations sequentially, and small blocks do not amortize kernel-launch overhead. The method is therefore most effective when the structured problem supplies enough independent, sufficiently large dense blocks at each reduction level.

### Contributions

1. Specialized recursive Schur-complement reduction for block-tridiagonal SPD systems on GPUs.
2. Mapped independent factorization and solve tasks to batched BLAS/LAPACK kernels.
3. Delivered a cross-platform implementation for NVIDIA and AMD accelerators.
4. Benchmarked against CHOLMOD, HSL MA57, and NVIDIA cuDSS.
5. Identified sequential recursion levels and kernel-launch amortization as the main performance limits.
