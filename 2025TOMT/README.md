# 2025TOMT

## ChatGPT (July 2026)

### Summary

Python's sparse-computing ecosystem often lacks portable high-performance kernels, advanced iterative solvers, and preconditioners. pyGinkgo provides a lightweight Python interface to the Ginkgo C++ linear-operator framework through Pybind11, exposing Reference, OpenMP, CUDA, HIP, and SYCL executors together with sparse matrices, solvers, and preconditioners. A Python dispatch layer hides C++ template instantiations, while the buffer protocol permits zero-copy NumPy exchange and interfaces support NumPy and PyTorch workflows. Benchmarks use SuiteSparse matrices on Intel Xeon CPUs, NVIDIA A100 GPUs, and AMD MI100 GPUs. For sparse matrix--vector multiplication, pyGinkgo outperforms SciPy, CuPy, PyTorch, and TensorFlow on the tested GPU cases and scales well across CPU threads. For iterative solvers, it beats CuPy for CG and CGS but CuPy is slightly faster for the tested GMRES configuration; CPU solvers also outperform SciPy. Comparison with native Ginkgo shows that relative binding overhead can be substantial for small matrices but falls below 10% for most cases above $10^7$ nonzeros on NVIDIA hardware, with small absolute timing differences. The framework therefore brings Ginkgo performance and portability to Python without hiding measured small-problem overheads or solver-specific trade-offs.

### Contributions

1. Exposed Ginkgo's portable sparse operators, executors, iterative solvers, and preconditioners through a Pythonic API.
2. Designed a dispatch layer that maps Python types to pre-instantiated C++ templates without expanding binding complexity unnecessarily.
3. Enabled efficient ecosystem interoperability through the Python buffer protocol and NumPy and PyTorch-compatible interfaces.
4. Benchmarked SpMV and iterative solvers across CPU, NVIDIA, and AMD hardware against major Python libraries.
5. Quantified Pybind11 overhead relative to native Ginkgo, showing low absolute cost and diminishing relative overhead for large sparse matrices.
