# 2026HBKW

## Codex/ChatGPT (September 2026)

### Summary

This paper reformulates plasma-fluid equations in general nonorthogonal
curvilinear coordinates so that geometric source terms need not appear
explicitly in the nonlinear kinetic stress. Density, momentum, and internal
energy are rescaled by the coordinate Jacobian, making conserved mass,
kinetic energy, and internal energy quadratic under ordinary Euclidean inner
products. For a resistive-magnetohydrodynamic testbed, antisymmetric first
derivatives and elementary dot- and cross-product identities are sufficient to
derive discrete mass, cyclic-coordinate angular-momentum, and total-energy
conservation. The ALMA implementation generates Fortran operators from symbolic
Python and uses centered finite differences with a staggered curl--curl
operator. Shercliff-flow tests show second-order convergence and large accuracy
gains from grid stretching; an Orszag--Tang vortex on a distorted grid retains
total energy to about 12 digits and magnetic solenoidality to about 11 digits.
The centered scheme can oscillate near sharp gradients, and computing metrics
with the same finite differences does not guarantee an exact discrete
geometric conservation law, which the authors identify as future work.

### Contributions

1. Recast the plasma-fluid hierarchy in Jacobian-weighted variables that conceal explicit geometric forces.
2. Derived coordinate-independent discrete conservation conditions based on antisymmetry and vector identities.
3. Applied the formulation to resistive magnetohydrodynamics with compatible viscosity and Ohmic heating.
4. Implemented symbolic-to-Fortran curvilinear operators in the ALMA finite-difference code.
5. Verified convergence and conservation on Shercliff flow and distorted-grid Orszag--Tang tests.
