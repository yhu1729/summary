# 2026MR

## ChatGPT (July 2026)

### Summary

This paper develops structure-preserving discretizations for three two-dimensional ideal magnetized-fluid models: reduced magnetohydrodynamics (RMHD), Hazeltine's three-field model, and the Charney-Hasegawa-Mima (CHM) equation. Each model has a non-canonical Hamiltonian formulation with Lie-Poisson geometry, Casimir invariants, and phase flows restricted to coadjoint orbits. The authors apply Zeitlin's matrix-hydrodynamics truncation and a compatible geometric time integrator so that finite-dimensional simulations retain this structure over long times. Randomized initial conditions reveal shared and model-specific turbulent organization. RMHD and Hazeltine dynamics form large-scale magnetic dipoles, and spectral diagnostics support inverse transfer of magnetic energy and mean-square magnetic potential. Their vorticity behavior differs sharply: RMHD develops thin filaments, growing vorticity, and a direct kinetic-energy cascade, whereas Hazeltine and CHM form large-scale vorticity structures with inverse kinetic-energy transfer and little vorticity-amplitude change. The comparison shows that structure-preserving numerics can expose distinct long-time statistics among closely related reduced plasma models.

### Contributions

1. Formulated compatible matrix-hydrodynamics discretizations for RMHD, Hazeltine, and CHM dynamics.
2. Combined the spatial truncations with a geometric time integrator that preserves the underlying Lie-Poisson structure.
3. Performed long-time turbulent simulations from randomized initial data across all three models.
4. Demonstrated inverse magnetic transfer and magnetic-dipole formation in RMHD and Hazeltine dynamics.
5. Distinguished RMHD's filamentation and direct kinetic cascade from the inverse kinetic cascades of Hazeltine and CHM models.
