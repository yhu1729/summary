# 2026NDLB

## ChatGPT (July 2026)

### Summary

This paper adapts the open-source EPOCH and Smilei particle-in-cell codes to model metals, semimetals, and nanoscale light--matter interactions as cold quantum plasmas. Four modules are presented: Fermi--Dirac carrier initialization; material-edge boundary conditions for spill-out, confinement, and scattering; bound macroparticles with damped-Lorentz forces for dispersive media; and massless Dirac carriers whose velocity is renormalized to the Fermi velocity. Benchmarks reproduce Fermi--Dirac relaxation trends, nonlocal surface-plasmon shifts, an FDTD Lorentz-medium response, silicon-nanopillar reflectance, persistent radiation from excited bound media, and analytical graphene-disk resonances. Because material components remain particles coupled self-consistently to Maxwell fields, the framework captures time-dependent media and surface dynamics that static dielectric models omit. Important limitations remain: the method is semiclassical, does not enforce Pauli exclusion during evolution, omits unresolved incoherent photon emission, and currently treats Dirac carriers at zero electronic temperature.

### Contributions

1. Implemented Fermi--Dirac particle initialization and quantified its resolution-dependent relaxation.
2. Added material-boundary models for electron spill-out, work-function confinement, and surface scattering.
3. Derived a modified Boris pusher for bound macroparticles in Lorentz-dispersive media.
4. Developed a constant-Fermi-speed PIC model and validated graphene-disk resonances.
5. Demonstrated self-consistent coupling with existing PIC physics and identified semiclassical limitations.
