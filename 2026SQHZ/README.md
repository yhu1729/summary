# 2026SQHZ

## ChatGPT (July 2026)

### Summary

This paper proposes an adaptive-rank solver for multiscale BGK kinetic equations based on greedy sampling and adaptive cross approximation. Instead of forming low-rank decompositions of nonlinear local Maxwellians, the method identifies important rows and columns of the solution matrix, advances only those samples with a high-order semi-Lagrangian local solver, and reconstructs the full solution through cross approximation. A locally macroscopic conservative correction enforces mass, momentum, and energy conservation by coupling the low-rank kinetic update to a high-order macroscopic system. The macroscopic equations use stiffly accurate DIRK time stepping and matrix-free Jacobian-free Newton-Krylov solves, with the provisional low-rank solution serving as a closure and initial guess. The paper proves a conditional asymptotic-preserving property and tests smooth, discontinuous, and mixed-regime problems spanning several Knudsen-number orders of magnitude. Results show strict conservation, high-order behavior, large-time-step capability, and linear scaling in one benchmark, with high-dimensional extensions and preconditioning left for future work.

### Contributions

1. Introduced a greedy adaptive-rank BGK solver that avoids explicit low-rank Maxwellian decompositions.
2. Used adaptive cross approximation to update selected rows and columns and reconstruct the kinetic solution.
3. Enforced mass, momentum, and energy through a locally macroscopic conservative correction.
4. Coupled semi-Lagrangian kinetic updates with DIRK and matrix-free Newton-Krylov macroscopic solves.
5. Demonstrated conservation, conditional asymptotic preservation, and performance across kinetic-fluid regimes.
