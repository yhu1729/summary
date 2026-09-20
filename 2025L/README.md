# 2025L

## ChatGPT (July 2026)

### Summary

The paper develops structure-preserving particle-in-cell methods for hybrid plasma models in which ions remain fully kinetic, electrons obey a Boltzmann relation, and a Poisson equation retains space-charge effects. Discretizing either the action integral or the noncanonical Poisson bracket yields equivalent finite-dimensional Hamiltonian systems. Hamiltonian splitting then gives symplectic time integrators, while discrete-gradient methods preserve the discrete energy exactly. Under periodic or homogeneous Neumann boundary conditions, the schemes also retain the model's global neutrality condition. The formulation is extended to an electromagnetic hybrid model with a slowly varying laser envelope. Numerical experiments covering finite-grid instability, Landau damping, and resonantly driven nonlinear ion waves demonstrate the methods' conservation behavior and dynamics; in a reported nonlinear-wave test, the discrete-gradient method maintains energy to near solver tolerance. The analysis focuses mainly on one-dimensional electrostatic examples, while higher-dimensional discretizations, other boundary conditions, and broader electromagnetic applications are left for future work.

### Contributions

1. Derived variational and Hamiltonian formulations for a kinetic-ion, Boltzmann-electron plasma model with space charge.
2. Constructed equivalent finite-dimensional Hamiltonian systems by discretizing the action and the Poisson bracket.
3. Developed symplectic Hamiltonian-splitting and energy-preserving discrete-gradient particle-in-cell integrators.
4. Proved preservation of global neutrality under suitable boundary conditions.
5. Extended the geometric formulation to an electromagnetic hybrid model and tested it on three plasma benchmarks.
