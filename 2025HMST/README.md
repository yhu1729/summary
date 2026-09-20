# 2025HMST

## ChatGPT (July 2026)

### Summary

This paper develops a finite-element scheme for the electrostatic Euler-Poisson equations with a prescribed constant magnetic field. The method targets the magnetic-drift regime, where smooth hydrodynamic motion coexists with plasma and cyclotron oscillations separated by more than ten orders of magnitude in time scale. An operator split treats the compressible Euler subsystem explicitly with a conservative, invariant-domain-preserving graph-viscosity method, while the stiff source subsystem is advanced implicitly. A PDE Schur complement eliminates the coupled momentum and Lorentz-force variables, reducing each source update to one nonsymmetric Poisson-like solve. At the fully discrete level, the authors prove positivity of density and internal energy, a minimum principle for specific entropy, and a total-energy balance. Numerical tests show that the scheme can operate near the magnetic-drift limit without resolving the fastest oscillations. A diocotron-instability calculation reproduces analytical growth rates and illustrates the approach on a demanding multiscale plasma problem. The construction is presented as a step toward similarly robust Euler-Maxwell solvers with self-consistent electric and magnetic fields.

### Contributions

1. Constructed a fully discrete finite-element scheme for the magnetic Euler-Poisson system.
2. Proved positivity, an entropy minimum principle, conservation properties, and a total-energy balance.
3. Split explicit invariant-domain Euler dynamics from an implicit treatment of stiff plasma and cyclotron motion.
4. Reduced the coupled source update to a single nonsymmetric Poisson-like problem through a PDE Schur complement.
5. Validated magnetic-drift behavior with a diocotron instability whose growth rates agree with analytical predictions.
