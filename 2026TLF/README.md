# 2026TLF

## ChatGPT (July 2026)

### Summary

Fully kinetic particle-in-cell (PIC) simulations often reduce the speed of light or ion-to-electron mass ratio to make multiscale calculations affordable, but these substitutions distort Coulomb collision rates. This paper derives separate scaling factors for electron-electron, ion-ion, electron-ion, and ion-electron collisions instead of applying one global correction. The construction matches total electron and ion relaxation rates to their respective electromagnetic timescales while preserving electron-ion energy equilibration and important transport properties within weakly collisional plasma theory. Binary Monte Carlo PIC benchmarks reproduce theoretical relaxation rates, and comparisons with fluid theory confirm the retained transport behavior. The scaling applies to nonrelativistic systems satisfying $m_iT_e/(m_eT_i) \gg 1$; relativistic effects remain future work. Because the method changes only collision-rate factors, it can be incorporated into existing collisional PIC and other kinetic codes while retaining the computational savings of artificial physical parameters.

### Contributions

1. Quantified how reduced light speed and mass ratio alter distinct inter- and intra-species collision processes.
2. Derived species-dependent collision-rate factors instead of a single global rescaling.
3. Preserved electron and ion relaxation times, energy equilibration, and key transport properties simultaneously.
4. Validated the scaling against theoretical relaxation rates using binary-collision PIC benchmarks.
5. Connected the kinetic correction to fluid transport theory and identified its nonrelativistic validity regime.
