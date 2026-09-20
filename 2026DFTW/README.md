# 2026DFTW

## ChatGPT (July 2026)

### Summary

The paper extends OSIRIS with a deterministic particle-grid model for field and electron-impact ionization. Electron macroparticles deposit MRBEB-based ionization-rate, energy-loss, and secondary-momentum contributions to grids; coupled charge-state rate equations are advanced deterministically, and electrons and ions are injected with conserved charge and modeled momentum. The implementation supports immobile neutral media and mobile ion macroparticles and augments tunneling field ionization with barrier-suppression corrections. Verification against analytical rate equations, stopping-power predictions, and momentum-transfer formulas covers several elements and charge states. Comparisons with Smilei and EPOCH show agreement after accounting for cross-section choices and expose inaccuracies in a multiple-ionization-per-timestep Monte Carlo treatment. Relative to particle-pair Monte Carlo schemes, the grid method reduces ionization-rate error by up to two orders of magnitude at moderate particles per cell while retaining linear runtime scaling. The current implementation is slower and omits recombination, excited-state kinetics, ion-frame Lorentz transforms, and secondary-electron angular scattering.

### Contributions

1. Introduced a deterministic particle-grid collisional-ionization algorithm for immobile media and mobile ion macroparticles in OSIRIS.
2. Integrated MRBEB cross sections, energy exchange, momentum transfer, and tunneling-to-barrier-suppression field-ionization rates.
3. Advanced coupled charge-state populations deterministically while injecting ionized particles with charge conservation and numerical safeguards.
4. Verified rates, stopping power, and secondary momentum and benchmarked the implementation against Smilei and EPOCH.
5. Demonstrated linear particle-count scaling and substantially faster error reduction than Monte Carlo sampling at moderate particle counts.
