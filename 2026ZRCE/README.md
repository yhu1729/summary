# 2026ZRCE

## ChatGPT (July 2026)

### Summary

This paper documents the horizontal, vertical, and tangential infrared (HIR, VIR, and TIR) diagnostics on the Tokamak à Configuration Variable. Their Equus 81k M cameras measure graphite-tile temperatures at standard rates near $200\,\mathrm{Hz}$ and, with reduced frames, above $10\,\mathrm{kHz}$. A two-stage calibration combines heated tiles and thermocouples with pixelwise non-uniformity corrections. The Python THEODOR code then solves a heat-diffusion inverse problem to infer perpendicular heat flux, parallel heat flux, and deposited power, while modeling a surface layer whose heat-transmission factor remains uncertain. New measurements of graphite properties replace older estimates: conductivity is $25$-$40\%$ higher below $500\,^{\circ}\mathrm{C}$, although resulting peak heat fluxes increase by less than $15\%$. A heated, inclined VIR valley tile and TIR rooftop tiles increase signal for fast transients. Long-pass filters suppress the dominant $4051\,\mathrm{nm}$ deuterium line, substantially reducing parasitic plasma light. VIR and TIR heat-flux profiles agree at low density after geometry correction, but VIR overestimates background power as density rises. Residual plasma emission and the surface-layer transmission factor therefore remain the leading diagnostic uncertainties.

### Contributions

1. Consolidated the geometry, operating modes, calibration, and performance limits of TCV's three infrared diagnostic systems.
2. Detailed the temperature-to-heat-flux workflow implemented in Python THEODOR, including surface-layer and magnetic-incidence corrections.
3. Measured temperature-dependent graphite density, heat capacity, diffusivity, and conductivity and quantified their effect on inferred heat flux.
4. Designed heated and inclined VIR and TIR tiles that increase infrared signal for high-frequency transient measurements.
5. Demonstrated the benefit and remaining limitations of $4095\,\mathrm{nm}$ long-pass filtering through cross-comparison of VIR and TIR heat fluxes.
