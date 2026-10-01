# 2015SHH

## ChatGPT (July 2026)

### Summary

This paper develops and benchmarks a one-dimensional electrostatic gyrokinetic model for parallel propagation of a JET-like edge-localized-mode heat pulse through the scrape-off layer to divertor plates. Gyrokinetic quasineutrality and logical-sheath boundary conditions remove the need to resolve the electron Debye length and plasma frequency while retaining kinetic electrons and ions. To make explicit calculations tractable, the authors modify the ion-polarization term with a minimum perpendicular wavenumber and derive the corresponding Hamiltonian correction required for energy conservation. A continuum discontinuous Galerkin implementation in Gkeyll uses a flux-balanced sheath cutoff and specified benchmark initial conditions. Its divertor heat-flux history agrees well with earlier Vlasov and full-orbit particle-in-cell results: fast electrons cause only an early modest signal because the rising sheath potential confines most electrons, and the bulk ELM energy reaches the target on the slower ion transit timescale. A Boltzmann-electron reduction reproduces the main heat pulse at much lower cost but omits early kinetic-electron effects.

### Contributions

1. Formulated an energy-consistent electrostatic gyrokinetic scrape-off-layer model with a modified polarization term.
2. Implemented logical-sheath boundary conditions that enforce zero net wall current without resolving the Debye sheath.
3. Supplied reproducible JET-like edge-localized-mode source and initial-condition specifications for kinetic-code benchmarks.
4. Matched prior Vlasov and full-orbit PIC heat-flux results and explained the ion-timescale bulk energy arrival.
5. Developed a faster Boltzmann-electron model and identified the kinetic-electron effects that it omits.
