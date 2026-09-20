# 2025PE

## ChatGPT (July 2026)

### Summary

Low-diffusion AUSM-family fluxes preserve stationary contacts and resolve shear and boundary layers accurately, but their weak dissipation can permit shock oscillations. The paper demonstrates that AUSM+, AUSM+-up, LDFSS(2), LDFSS-2001, and SLAU2 can become unstable when shocks are not aligned with unstructured tetrahedral meshes, even at low Mach number; it also exposes carbuncle behavior in AUSM+-up on unstructured meshes. To stabilize AUSM+ and LDFSS, three subsonic-only corrections add dissipation through velocity-jump scaling (2025u), pressure-jump scaling (2025p), or modified Mach splitting (2025M). Each correction vanishes for stationary contacts and retains pressure equilibrium across moving contacts and total-enthalpy preservation. Tests in the Quinoa hydrodynamics solver cover colliding streams, contact and shear waves, expansion, Mach-6 duct shocks, Mach-6 and Mach-20 blunt bodies, and a viscous double-ramp flow. The modifications suppress post-shock oscillations and avoid carbuncles in the tested cases. The velocity variant is most dissipative and robust; the Mach-splitting variant preserves shear layers best but leaves mild oscillations; the pressure variant offers the preferred balance. The most dissipative correction remains less diffusive than Van Leer flux-vector splitting. The analysis focuses on flux corrections and mostly first-order discretizations; grid-structure effects and a definitive carbuncle cause remain unresolved.

### Contributions

1. Demonstrated that shock-mesh misalignment can destabilize several low-diffusion AUSM-family schemes independently of shock strength and exposed AUSM+-up carbuncles on uniform unstructured meshes.
2. Introduced velocity-, pressure-, and Mach-splitting-based subsonic dissipation mechanisms for stabilizing AUSM+ and LDFSS fluxes.
3. Established that the modified schemes exactly preserve stationary contacts, pressure equilibrium across moving contacts, and total enthalpy.
4. Validated the modifications across colliding-flow, contact, shear, expansion, duct-shock, blunt-body, and viscous double-ramp benchmarks, with no carbuncles in the shock tests.
5. Quantified the robustness-diffusion trade-off among the three corrections and identified the pressure-based variant as the preferred compromise.
