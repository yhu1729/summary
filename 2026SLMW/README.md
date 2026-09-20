# 2026SLMW

## Codex/ChatGPT (September 2026)

### Summary

ORB5X is a C++17/Kokkos translation of the global electromagnetic gyrokinetic
particle-in-cell code ORB5. It retains ORB5's variational gyrokinetic model,
$\delta f$ marker particles, B-spline field representation, Fourier filtering,
MPI toroidal decomposition and cloning, and HDF5 diagnostics while replacing
Fortran, OpenMP, and OpenACC data and kernels with typed C++ objects and Kokkos
Views. The authors used coding agents for bounded translation tasks, followed
by human review and staged CPU, GPU, and multi-GPU validation. ITG, ITPA, and
chirping benchmarks reproduce ORB5 fields and diagnostics to near machine
precision. Strong-scaling tests extend to 2,048 AMD GPUs on LUMI-G and Alps,
with near-ideal scaling in selected regimes and execution across laptops and
multiple clusters. The work establishes a portable, maintainable baseline
rather than a new physical model: the original Fortran code remains faster
where available, and some FFTW, HDF5, LAPACK, and MPI paths still stage data on
the host.

### Contributions

1. Reimplemented ORB5's electromagnetic gyrokinetic PIC algorithm in C++17 with Kokkos portability.
2. Preserved the established MPI decomposition, particle cloning, and HDF5 diagnostics across the translation.
3. Defined a human-supervised agentic workflow with bounded patches and progressively broader validation.
4. Demonstrated numerical agreement with ORB5 on ITG, ITPA, and chirping benchmarks.
5. Evaluated portability and strong scaling through 2,048 GPUs while identifying remaining host-staged operations.
