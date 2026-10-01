# 2025BOMG

## ChatGPT (July 2026)

### Summary

$\pi$-PIC is a Python-controlled framework for developing, combining, and comparing particle-in-cell (PIC) algorithms without embedding every experiment in a monolithic code. A precompiled C++ core, exposed through pybind11, stores particles cell by cell and supports multithreading, while Python callbacks and modular extension and solver interfaces permit rapid experimentation without moving performance-critical work into Python. The paper demonstrates extensions for masked absorbing boundaries, moving windows, and mapping tightly focused laser pulses into smaller periodic domains. It also implements several solvers, including a simple electrostatic example and a second-order explicit energy-conserving method modified to reduce momentum error. In laser-wakefield benchmarks, the energy-conserving and Fourier-Boris solvers give similar plasma responses. Compared with Smilei, $\pi$-PIC retains greater qualitative accuracy at coarse resolution, but converges more weakly as resolution increases; the authors attribute the remaining discrepancy primarily to particle shape functions. The framework currently lacks multi-node and GPU execution, so its contribution is a modular research platform rather than a replacement for mature production-scale PIC codes.

### Contributions

1. Defined a unified Python/C++ interface that separates simulation control, reusable extensions, and interchangeable PIC and field solvers.
2. Designed a thread-aware execution model that lets independently developed extensions access particles and fields while remaining compatible with multiple solvers.
3. Implemented and tested reusable extensions for absorbing boundaries, moving windows, and tightly focused laser-pulse mapping.
4. Extended an explicit energy-conserving PIC solver with corrections that eliminate two identified sources of momentum error.
5. Benchmarked $\pi$-PIC against Smilei in laser-wakefield acceleration, exposing complementary low-resolution accuracy and high-resolution convergence behavior.
