# 2026ZGZ

## ChatGPT (July 2026)

### Summary

The authors develop a predictor--corrector discrete unified gas kinetic scheme (PRC-DUGKS) for Boltzmann transport equations containing both conservative and non-conservative collisions. Unlike standard DUGKS, the method directly advances the original distribution function, so macroscopic moments and boundary conditions remain well defined when absorption, fission, or other non-conservative processes are present. A unified trapezoidal predictor--corrector treatment removes the implicit coupling without introducing the splitting errors of Strang-split DUGKS. Multigroup neutron-transport tests range from one-group problems to the TWIGL benchmark and pin-resolved mixed-oxide reactor cores. PRC-DUGKS captures steep flux and power profiles with large time steps and consistently improves on the split formulation near strong absorbers. In the reported reactor tests it attains comparable or better accuracy while providing speedups of about $2.6\times$ for TWIGL and roughly $11\times$ for the full-core cases.

### Contributions

1. Extended DUGKS to transport models combining conservative and non-conservative collision operators.
2. Directly evolved the physical distribution function, enabling consistent moment recovery and boundary treatment.
3. Coupled transport and collision processes with a second-order predictor--corrector update without operator splitting.
4. Validated the scheme on multigroup neutron benchmarks from simple media to pin-resolved reactor cores.
5. Demonstrated improved large-step accuracy and substantial speedups over Strang-split DUGKS.
