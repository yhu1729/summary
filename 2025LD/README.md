# 2025LD

## ChatGPT (July 2026)

### Summary

Lucca and Dumbser construct finite-volume discretizations for nonlinear symmetric-hyperbolic and thermodynamically compatible systems, where total energy is a structural conservation law and many models also carry stationary involution constraints. The paper first presents a collocated, cell-centered HTC scheme that is compatible with semi-discrete energy conservation but does not generally preserve discrete vector-calculus identities. Its main contribution is a staggered, vertex-based, semi-implicit scheme written in discrete Godunov form. Compatible mimetic operators make $\nabla \cdot \nabla \times A = 0$ and $\nabla \times \nabla \phi = 0$ hold exactly at the fully discrete level, while the implicit solve reduces to symmetric positive-definite linear systems inside a fixed-point iteration. Tests on nonlinear acoustics, nonlinear Maxwell equations, and nonlinear Maxwell-GLM equations show exact total-energy conservation and exact preservation of the relevant divergence or curl involutions for the staggered method.

### Contributions

1. Developed structure-preserving finite-volume schemes for nonlinear SHTC systems.
2. Separated energy-compatible collocated discretization from fully compatible staggered discretization.
3. Built a semi-implicit Godunov-form method leading to symmetric positive-definite linear systems.
4. Preserved discrete vector-calculus identities exactly through compatible mimetic operators.
5. Verified conservation and involution preservation on nonlinear acoustic and Maxwell-type systems.
