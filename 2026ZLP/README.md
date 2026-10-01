# 2026ZLP

## ChatGPT (July 2026)

### Summary

This paper links loss of pressure and internal-energy positivity in low-$\beta$ magnetohydrodynamic calculations to inconsistency between reconstructed magnetic fields and energies inside HLL-family Riemann fans. It imposes an intermediate-state condition requiring total energy to equal the sum computed from the same density, momentum, and magnetic field. The resulting HLLC-ec solver adopts a revised two-state approximation that improves magnetic-field accuracy at the cost of contact resolution; HLLD-ec replaces constant total pressure with three intermediate thermal-energy states. Analytical examples and one- and two-dimensional tests show similar ordinary shock resolution but substantially smaller false waves, density dips, internal-energy errors, and divergence errors in difficult low-$\beta$ cases. HLLD-ec survives some extreme tests in which the classical solver fails, although both can still break down when uncontrolled multidimensional divergence error grows. The formulation addresses conservative ideal MHD only, does not replace a divergence-control method, and does not isolate every modification's individual effect. HLLC-ec is also more diffusive across fluid contacts.

### Contributions

1. Identified inconsistent intermediate magnetic fields and energies as a route to negative internal energy.
2. Formulated a general intermediate-state energy-consistency condition for HLL-family solvers.
3. Derived an energy-consistent HLLC variant prioritizing magnetic accuracy.
4. Derived an HLLD variant with three consistent intermediate thermal-energy states.
5. Connected state inconsistency to time-integrated errors and reduced low-$\beta$ numerical failures.
