# 2026AMC

## ChatGPT (July 2026)

### Summary

This paper derives a locally conservative spatial discretization of the compressible Euler equations for thermally perfect gases, whose heat capacities vary with temperature. The numerical flux exactly conserves discrete thermodynamic entropy, mass, momentum, and total energy while preserving kinetic energy. By exploiting the thermally perfect equation of state, the formulation removes singular terms that arise in a generic real-gas entropy-conservative flux; only logarithmic means remain. The framework accommodates different caloric models and multicomponent nonreacting mixtures, extends to arbitrary spatial order, and yields an asymptotically entropy-conservative hierarchy through Taylor expansion. Tests with periodic jets, a three-dimensional Taylor--Green vortex, and a shock tube verify conservation and show improved kinetic-energy evolution and small-scale statistics relative to comparable entropy-conservative schemes. Local Lax--Friedrichs dissipation supplies shock-capturing robustness when discontinuities are present.

### Contributions

1. Derived an exactly entropy-conservative flux for thermally perfect-gas Euler equations.
2. Preserved primary invariants and kinetic energy within the same locally conservative discretization.
3. Removed generic real-gas flux singularities by using the structure of thermally perfect equations of state.
4. Extended the construction to high order, multicomponent mixtures, and asymptotically entropy-conservative approximations.
5. Demonstrated improved robustness and kinetic-energy fidelity on two- and three-dimensional flow tests.
