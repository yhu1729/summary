# 2026DBCT

## ChatGPT (July 2026)

### Summary

The paper develops a communication-avoiding $s$-step preconditioned conjugate-gradient method for distributed GPU systems. It builds each block Krylov basis with Chebyshev polynomials and solves the resulting small Gram systems approximately using forward Gauss-Seidel sweeps, reducing global synchronizations while retaining practical numerical stability. A moment representation explains why the Chebyshev Gram matrix remains reasonably conditioned for moderate block sizes, and the equivalence between forward Gauss-Seidel and modified Gram-Schmidt provides a structural justification for the inner iteration. A performance model makes explicit the trade-off between fewer global reductions and extra local arithmetic. Multi-GPU tests on three-dimensional Poisson systems show improved strong scaling relative to classical CG. Weak-scaling experiments with algebraic multigrid exceed four billion unknowns; at 512 GPUs, $s=2,3,4$ reduce time to solution, with $s=4$ giving the best tested balance. The authors limit these conclusions to the explored scales and propose adaptive Gram-solve accuracy and communication-reducing preconditioners for larger systems.

### Contributions

1. Combined a Chebyshev block basis with iterative forward Gauss-Seidel Gram solves in $s$-step PCG.
2. Related Gram conditioning to a moment structure and the inner solve to modified Gram-Schmidt.
3. Derived a performance model balancing synchronization savings against additional local work.
4. Implemented and evaluated the method on NVIDIA A100 and H100 multi-GPU systems.
5. Demonstrated convergence beyond four billion unknowns and weak-scaling gains at 512 GPUs for moderate $s$.
