# 2025E

## ChatGPT (July 2026)

### Summary

The Dirichlet--Neumann alternating method is well understood for linear elliptic equations, but general convergence results for nonlinear, nonoverlapping decompositions were largely restricted to one dimension. This paper proves local linear convergence for a class of semilinear elliptic equations on Lipschitz domains in two and three dimensions without cross-points. It first establishes an abstract convergence theorem for nonlinear preconditioned iterations in Hilbert spaces. The domain-decomposition iteration is then written through nonlinear Steklov--Poincaré interface operators, whose differentiability, Lipschitz continuity, symmetry of derivatives, and uniform monotonicity provide the theorem's hypotheses. For a sufficiently small relaxation parameter and an initial interface guess sufficiently near the solution, both interface and subdomain iterates converge linearly. Finite-element experiments confirm mesh-independent rates on two nonlinear examples; they also show faster convergence than Robin--Robin iteration, while Neumann--Neumann fails on one example. Convergence degrades as the number of subdomains increases, motivating a future nonlinear coarse correction.

### Contributions

1. Proved convergence of the Dirichlet--Neumann method for semilinear elliptic problems in two and three dimensions.
2. Established a reusable local linear-convergence theorem for nonlinear Hilbert-space iterations.
3. Characterized the required nonlinear Steklov--Poincaré operators and their derivatives.
4. Transferred interface convergence to the corresponding subdomain solutions.
5. Demonstrated mesh-independent finite-element convergence and compared competing nonoverlapping methods.
