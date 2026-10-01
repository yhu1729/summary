# 2026AR

## ChatGPT (July 2026)

### Summary

Entropy-stable discretizations improve robustness for hyperbolic systems, but constructions for nonconservative products often require path integrals or problem-specific derivations. The paper recasts Tadmor-type entropy conditions algebraically and proves necessary and sufficient conditions for entropy conservation or stability without requiring a convex entropy. It proposes four concrete fluctuation-based semi-discretizations of nonconservative terms and fully characterizes their entropy properties for three-point finite-volume methods. These forms enable algorithmic construction of affordable fluxes without evaluating path integrals. Applications recover existing constructions and derive new schemes for systems including variable-coefficient advection, shallow-water models, ideal magnetohydrodynamics, and compressible Euler equations written with internal energy. The paper then extends the finite-volume construction to high-order summation-by-parts operators on Cartesian and curvilinear meshes, carrying well-balanced properties from the underlying finite-volume method under stated conditions. Numerical tests verify accuracy, robustness, entropy behavior, and preservation of selected steady states. The results provide a general construction framework, while each application still requires compatible entropy variables, fluctuations, and dissipation.

### Contributions

1. Proved algebraic necessary-and-sufficient entropy conditions that also apply to nonconvex functionals.
2. Characterized four practical fluctuation forms for nonconservative three-point finite-volume schemes.
3. Enabled algorithmic construction of entropy-conservative and entropy-stable fluxes without path-integral evaluation.
4. Extended the framework to multidimensional high-order summation-by-parts methods on Cartesian and curved meshes.
5. Recovered existing constructions and derived new entropy-preserving schemes for representative hyperbolic systems.
