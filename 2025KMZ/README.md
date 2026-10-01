# 2025KMZ

## ChatGPT (July 2026)

### Summary

The proximal Galerkin method combines a finite-element discretization with a proximal-point algorithm for variational problems subject to pointwise inequality constraints. This paper gives its first abstract a priori error analysis for quadratic optimization problems in Sobolev spaces. The framework treats discretization and iteration errors together rather than analyzing only linearized subproblems. It establishes checkable conditions for existence and uniqueness of the proximal subproblems, monotonic decrease of the objective, best-approximation properties, convergence rates, and asymptotic mesh-independent iteration complexity. The analysis also preserves feasibility at the discrete level and does not require a penalty parameter to approach a singular limit. The authors apply the theory to obstacle and Signorini contact problems using several conforming finite-element pairs and construct the stability and approximation operators needed by the abstract results. For the lowest-order conforming approximations covered by the proof, the resulting estimates attain optimal convergence rates. The work supplies a general mathematical foundation for the method while identifying high-order spaces and nonquadratic energies as important extensions beyond the present theory.

### Contributions

1. Presented the first abstract a priori error framework for the proximal Galerkin method.
2. Unified iteration and spatial-discretization errors for pointwise-constrained quadratic variational problems.
3. Proved objective decrease, best-approximation properties, convergence rates, and asymptotic mesh independence.
4. Derived optimal error estimates for lowest-order obstacle and Signorini finite-element discretizations.
5. Established convergence without singular penalty limits while retaining constraint-preserving approximations.
