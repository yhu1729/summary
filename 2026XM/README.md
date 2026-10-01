# 2026XM

## ChatGPT (September 2026)

### Summary

Discontinuous Galerkin spectral element implementations need consistent interface fluxes across element shapes, basis choices, and differing polynomial orders. The authors analyze two ways to evaluate nonconforming interfaces in a general Nektar++ framework. A shared trace space gives both sides the same quadrature and flux evaluation, preserving the symmetry needed by conjugate-gradient solves of symmetric interior-penalty Helmholtz systems. Point-to-point interpolation can be cheaper, but inconsistent interface evaluation can make the matrix nonsymmetric. Their matrix-free workflow keeps most operations in physical space and limits expensive transforms to one backward transform and one inner product. CPU implementations reuse cached data and vectorize batches across hexahedra, prisms, and tetrahedra. Benchmarks compare interface strategies, polynomial orders, and element types; interpolation is faster than trace inner products but carries the stated numerical caveat. The study treats polynomial nonconformity, with geometric nonconformity left for future work.

### Contributions

1. Identified how inconsistent nonconforming flux evaluation breaks interior-penalty matrix symmetry.
2. Developed shared-trace and point-to-point interface strategies for general spectral elements.
3. Reduced coefficient--physical transforms in a matrix-free discontinuous Galerkin workflow.
4. Implemented cache reuse and SIMD batching for several unstructured element shapes in Nektar++.
5. Measured CPU throughput and exposed the speed--symmetry trade-off between interface strategies.
