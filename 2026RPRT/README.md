# 2026RPRT

## ChatGPT (July 2026)

### Summary

This study models runaway-electron heating of a realistic, though not final, tungsten-heavy-alloy tile from SPARC's outboard off-midplane limiter. A one-way workflow combines parametric and DREAM energy--pitch distributions, Geant4 volumetric energy deposition, and MEMENTO heat transfer for 1 and $10\,\mathrm{ms}$ loads. Curvature, magnetic-field inclination, finite Larmor radii, and redeposition of backscattered electrons produce three-dimensional energy partitioning that cannot be reproduced by a simple $\sin\alpha$ optical model or a single representative electron energy and pitch. At $20\,\mathrm{kJ}$, electrons of $10\,\mathrm{MeV}$ or more do not melt the limiter, whereas approximately $1\,\mathrm{MeV}$ electrons can melt about $100\,\mu\mathrm{m}$. At $100\,\mathrm{kJ}$, high-energy populations produce melt depths from several hundred micrometres to roughly $1\,\mathrm{mm}$; low-energy loading over $10\,\mathrm{ms}$ can vaporize about $500\,\mu\mathrm{m}$. DREAM distributions predict roughly $1\,\mathrm{mm}$ melting on the curved tile side. The model omits the complete viscoplastic, hydrodynamic, and fracture response required to predict explosive damage.

### Contributions

1. Built a SPARC-specific DREAM--Geant4--MEMENTO workflow with realistic limiter geometry and temperature-dependent alloy properties.
2. Compared two DREAM avalanche models and demonstrated why full energy--pitch distributions matter.
3. Quantified curvature, inclination, Larmor-radius, and backscatter-redeposition effects absent from simple optical models.
4. Mapped melting and vaporization across incident energies, pitches, total loads, and deposition times.
5. Resolved particle-loss channels and showed that high-energy photon losses require assessment of surrounding structures and magnets.
