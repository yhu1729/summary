# 2025HBCC

## ChatGPT (July 2026)

### Summary

This paper introduces Entity, an open-source particle-in-cell code for plasma astrophysics, and focuses on its curvilinear special-relativistic module. The code targets performance portability across GPU and CPU architectures through Kokkos while preserving an interface intended to be usable and customizable without modifying core internals. The module solves the Vlasov--Maxwell system in general coordinates, enabling coordinate-agnostic simulations in Cartesian, axisymmetric spherical, quasi-spherical, and future geometries. A central numerical choice is to advance particle equations of motion in a global orthonormal Cartesian basis even when fields and grids use generalized coordinates, improving stability. Charge conservation is maintained through conformal current deposition. The implementation is validated on standard Cartesian plasma tests and relativistic magnetosphere simulations in curvilinear axisymmetric geometries. Performance results show portability across AMD, NVIDIA, and Intel GPU platforms, with efficient particle push and current deposition kernels.

### Contributions

1. Presented Entity as a hardware-agnostic open-source PIC code for plasma astrophysics.
2. Implemented a general-coordinate special-relativistic Vlasov--Maxwell module.
3. Advanced particles in a global orthonormal basis to improve curvilinear-grid stability.
4. Preserved charge conservation with conformal current deposition.
5. Validated accuracy and performance portability across standard tests and multiple GPU platforms.
