# 2026DRM

## ChatGPT (July 2026)

### Summary

This paper develops a compressible dynamic forcing strategy that accelerates the transition from an upstream Reynolds-averaged Navier--Stokes solution to wall-modelled large-eddy simulation on curvilinear grids. The method amplifies wall-normal velocity fluctuations supplied by a synthetic turbulence generator, with density and forcing scalings derived from Morkovin's hypothesis and the Van Driest transformation. The generator can operate as an inlet boundary condition or as a volumetric source embedded inside the domain. In a Mach-2 zero-pressure-gradient boundary layer spanning $1000\leq Re_\tau\leq2500$, the combined method recovers skin friction within 5% of the Coles--Fernholz correlation after roughly 7--8 inlet boundary-layer thicknesses and shortens adaptation distance by as much as 70% relative to synthetic turbulence alone. A Mach-4.14 rounded-base calculation shows that resolved upstream turbulence is essential when the separated mixing layer has $M_c\approx1$: the method reproduces experimental shock, recirculation, mixing-layer, and base-pressure behavior that a RANS-inlet hybrid calculation misses.

### Contributions

1. Formulated compressible dynamic forcing with Morkovin and Van Driest scaling.
2. Supported synthetic turbulence as either an inlet condition or an embedded source.
3. Reduced Mach-2 boundary-layer adaptation distance by up to 70% without downstream artifacts.
4. Showed that hypersonic $M_c\approx1$ mixing layers require resolved upstream turbulence.
5. Validated the embedded RANS-to-WMLES strategy against rounded-base experiments.
