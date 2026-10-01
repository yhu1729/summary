# 2026AFKP

## ChatGPT (July 2026)

### Summary

This paper formulates particle resampling as a projection through a finite-element function space. Particle weights are first deposited into the continuum basis; a pseudoinverse particle mass matrix then transfers that representation to a freely selected replacement particle set. Because new particle locations and counts are decoupled from the continuum mesh, both discretizations can in principle adapt independently. The projection exactly preserves every moment representable by the finite-element polynomial space, including kinetic energy when quadratic velocity elements are used, and leaves the continuum field solve unchanged. A matrix-free LSQR implementation in PETSc-PIC is tested on $1X+1V$ Vlasov--Poisson two-stream instability and linear and nonlinear Landau damping. Resampling restores well-populated phase-space grids, suppresses particle noise, and sustains coherent dynamics to long times while preserving energy to solver tolerance. However, excessive resampling can smooth filaments, change vortex-merger timing, or trigger oscillatory instability. Tests use structured static grids and remap mainly to the original particle layout; stability analysis, adaptive unstructured meshes, optimized high-dimensional operators, and physically realistic $2X+3V$ cases remain future work.

### Contributions

1. Expressed conservative resampling as finite-element deposition followed by pseudoinverse projection.
2. Proved preservation of all moments represented by the chosen polynomial basis.
3. Decoupled replacement-particle placement and count from the continuum mesh.
4. Implemented a matrix-free PETSc-PIC solver with practical oversampling conditions.
5. Quantified noise reduction, conservation, and long-time behavior in kinetic benchmarks.
