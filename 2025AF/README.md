# 2025AF

## ChatGPT (July 2026)

### Summary

Numerical time integrators often preserve one invariant but cannot simultaneously enforce several conservation laws and dissipation inequalities. This paper presents a general auxiliary-variable framework for semidiscrete initial-value problems. Each quantity of interest is represented by an associated test function; projecting these functions onto the discrete test space defines auxiliary variables that modify the weak equations. The resulting arbitrary-order schemes reproduce multiple invariants and dissipation structures without reparametrizing the state to make them linear. For incompressible Navier--Stokes equations, the construction generalizes an energy-dissipating, helicity-tracking method to arbitrary temporal order. For compressible Navier--Stokes equations, it yields a time discretization that conserves mass, momentum, and energy while provably dissipating entropy. The framework also covers multiconservative Hamiltonian ordinary and partial differential equations. Reproducible implementations use Firedrake, PETSc, and MUMPS. The main practical limitation is the large coupled nonlinear system created by multiple auxiliary variables and high-order implicit stages, making scalable solvers an important next step.

### Contributions

1. Formulated a general test-function representation of conservation laws and dissipation inequalities.
2. Introduced projected auxiliary variables that enforce several structures simultaneously.
3. Generalized energy-dissipating and helicity-tracking incompressible-flow schemes to arbitrary order.
4. Derived a compressible-flow integrator conserving mass, momentum, and energy while dissipating entropy.
5. Supplied reproducible software and identified coupled nonlinear solution as the central performance challenge.
