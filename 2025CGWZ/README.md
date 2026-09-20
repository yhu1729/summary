# 2025CGWZ

## ChatGPT (July 2026)

### Summary

Strong nonlinearities make direct finite-element solves of variational PDEs expensive and can restrict Newton methods to local convergence. The DualTPD framework first applies Fenchel--Rockafellar duality to separate nonlinear constitutive terms from differential operators. Mixed finite elements place the nonlinear variable in a discontinuous space, producing element-local block-diagonal mass matrices with closed-form Jacobians and inverses. A transformed primal--dual iteration then improves the monotonicity of the saddle-point dynamics, while elliptic Schur complements are handled by problem-specific multigrid preconditioners. Unlike a nested Newton solve, linearization and solution proceed in one globally convergent iteration. Experiments on elliptic $p$-Laplacian and nonlinear $H(\mathrm{curl})$ problems report global, mesh-independent convergence and strong gains over primal formulations in highly nonlinear cases. The paper establishes the algorithmic framework and numerical evidence; a complete convergence analysis is deferred.

### Contributions

1. Introduced DualTPD, a duality-based preconditioning framework for nonlinear variational PDEs.
2. Decoupled nonlinear and differential operators through Fenchel--Rockafellar duality.
3. Used discontinuous mixed finite elements to obtain element-local nonlinear updates and inverses.
4. Combined transformed primal--dual dynamics with multigrid-preconditioned elliptic Schur complements.
5. Demonstrated global, mesh-independent convergence for $p$-Laplacian and nonlinear $H(\mathrm{curl})$ problems.
