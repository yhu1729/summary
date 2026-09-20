# 2026KSCP

## ChatGPT (July 2026)

### Summary

Tadmor's entropy-conservative flux condition applies to convex conserved secondary quantities, but real-gas simulations also need non-convex or non-conservative structures such as kinetic energy. This paper derives continuous and discrete compatibility conditions for secondary balance laws that may contain work terms. Singular Hessians and non-injective gradients introduce a necessary property called null-consistency: admissible work terms must vanish along null directions for the generalized flux condition to be well posed. Discrete-gradient operators then provide systematic jump expansions even when thermodynamic functions are supplied by an arbitrary equation of state rather than closed formulas. Applying the framework to the Euler equations yields KEEP-DG, an entropy-conserving and kinetic-energy-consistent flux for general equations of state that removes a singularity in an earlier construction. Supercritical and transcritical tests, including turbulent flow with detailed thermodynamics and transport, remain stable and conservative to machine precision on the tested grids. The theory is developed for smooth solutions; pressure-equilibrium preservation is left for future work.

### Contributions

1. Generalized continuous and discrete Tadmor compatibility conditions beyond convex entropy pairs.
2. Identified null-consistency as necessary for well-posed secondary-structure-preserving fluxes.
3. Used discrete gradients to construct fluxes for implicitly specified real-gas thermodynamics.
4. Derived the singularity-free KEEP-DG flux for arbitrary equations of state.
5. Demonstrated robust, machine-precision conservation in supercritical and transcritical flow tests.
