# 2026DJUN

## ChatGPT (July 2026)

### Summary

OpenEdge is an open-source DSMC framework for plasma-material interaction and charged-particle transport in magnetic-fusion environments. Rather than replacing SPARTA, it builds domain-specific fusion capabilities on SPARTA's DSMC engine, adding charged-particle transport, Coulomb collisions, ionization and recombination, sputtering and reflection models, sheath effects, and coupling to plasma backgrounds. The implementation uses object-oriented C++ with a Python interface and Kokkos-enabled parallelism for modern high-performance platforms. Verification and validation examples test collision operators, ionization, sheath behavior, impurity transport, and quantitative comparisons with WEST facility data. The paper positions OpenEdge as a modular tool for whole-device and edge-plasma studies where kinetic impurity and surface physics matter. Current limitations are also clear: predictive use depends on external background plasma data and ongoing development of dynamic surface evolution, re-erosion, evaporation, charging, and changing-field models.

### Contributions

1. Introduced OpenEdge as a fusion-oriented DSMC framework built on the SPARTA engine.
2. Added PMI physics modules for collisions, ionization, recombination, reflection, sputtering, and sheath effects.
3. Provided a C++/Python software architecture with Kokkos-based parallel execution support.
4. Verified key physics components and compared impurity-transport behavior with WEST observations.
5. Defined development paths for dynamic surfaces, deposited layers, lithium droplets, and evolving plasma backgrounds.
