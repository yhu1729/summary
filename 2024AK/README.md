# 2024AK

## ChatGPT (July 2026)

### Summary

Arya and Kalyanaraman construct an implicit leapfrog family of arbitrary even temporal order $R$ for a three-field $(p,E,H)$ formulation of Maxwell's equations, where the auxiliary pressure enforces the electric divergence constraint. The method, denoted $LF_R$, uses staggered time grids and operator corrections generated from Taylor expansions; a specialized half-step initialization preserves the designed order. Coupling $LF_R$ to compatible simplicial finite elements from a discrete de Rham sequence maintains the differential structure among scalar, electric, and magnetic fields. The analysis proves exact conservation of the weighted discrete energy for sufficiently small fixed time steps. Under regularity assumptions, the time-semidiscrete error is $O(\Delta t^R)$, while the fully discrete error is bounded by $O(\Delta t^R+h^r+h^r\Delta t^R)$ for Whitney-form polynomial order $r$. Two two-dimensional manufactured-solution experiments test the sixth-order member with linear and quadratic Whitney elements, including a case with nonzero pressure and nonhomogeneous boundary data. The work generalizes the authors' earlier second- and fourth-order schemes into one structure-preserving framework.

### Contributions

1. Defined an arbitrary-even-order implicit staggered leapfrog family $LF_R$ for the three-field Maxwell system, including consistent startup equations.
2. Proved exact conservation of the weighted discrete $p$--$E$--$H$ energy for the time-semidiscrete method.
3. Established $R$th-order temporal convergence under stated regularity assumptions.
4. Coupled the scheme to compatible simplicial de Rham finite elements and proved a full space--time error bound.
5. Validated the sixth-order method on two analytical Maxwell problems with linear and quadratic Whitney bases.
