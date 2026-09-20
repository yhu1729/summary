# 2026CH2

## ChatGPT (July 2026)

### Summary

This paper systematizes the construction of conforming three-dimensional finite element complexes through the Bernstein-Gelfand-Gelfand framework. Direct discretization is obstructed because the $H^1$, $H(\mathrm{curl})$, and $H(\mathrm{div})$ rows in a BGG diagram have incompatible continuity and some inter-row maps lack discrete right inverses. The authors introduce two reduction operations and an augmentation operation on exact sequences, then apply them to smooth finite element de Rham complexes. This produces broad families of exact Hessian, elasticity, and $\mathrm{div}\,\mathrm{div}$ complexes parameterized by vertex-, edge-, and face-smoothness vectors. Concrete finite element descriptions and unisolvent degrees of freedom are obtained using tangential-normal decomposition, face trace complexes, two-dimensional analogues, and bubble polynomial complexes. The work unifies several earlier case-specific constructions and supplies new conforming complexes without proposing a particular PDE solver.

### Contributions

1. Formulated two reduction operations and one augmentation operation that overcome continuity mismatches in discrete BGG diagrams.
2. Derived parameterized exact three-dimensional finite element Hessian complexes.
3. Constructed exact finite element elasticity complexes and identified their symmetric-tensor spaces and operators.
4. Constructed exact finite element $\mathrm{div}\,\mathrm{div}$ complexes, including reduced-smoothness variants.
5. Supplied explicit unisolvent degrees of freedom using tangential-normal decompositions, trace complexes, and bubble-space exactness.
