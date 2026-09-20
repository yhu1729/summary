# 2026KLWB

## ChatGPT (July 2026)

### Summary

This paper combines Numerical Flow Iteration (NuFI) with the Characteristic Mapping Method (CMM) for the 1D+1V Vlasov--Poisson system. NuFI supplies symplectic, conservative local evolution through a compact electric-field representation, while periodically stored CMM submaps limit the growing cost of repeatedly tracing characteristics. The hybrid reconstructs the distribution from a composed backward map and permits the map grid to be much coarser than the sampling grid. Landau-damping and two-stream-instability experiments reproduce expected dynamics and resolve fine phase-space filamentation. Relative to classical CMM, the method improves mass, energy, and norm behavior; relative to plain NuFI, remapping sharply reduces runtime, with the best tested balance near 20 NuFI steps per remap. Compared with a cubic semi-Lagrangian predictor--corrector, flow mapping preserves the $L^2$ and maximum norms and momentum substantially better, although the baseline conserves mass better.

### Contributions

1. Introduced a hybrid CMM--NuFI backward-flow-map algorithm for Vlasov--Poisson dynamics.
2. Combined symplectic NuFI local stepping with CMM submap composition for cheaper long-time propagation.
3. Separated coarse map storage from fine distribution sampling to provide high effective phase-space resolution.
4. Derived memory and computational-cost models exposing the remapping-frequency trade-off.
5. Validated conservation, accuracy, fine-structure resolution, and runtime against three baseline schemes.
