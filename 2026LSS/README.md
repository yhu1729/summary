# 2026LSS

## ChatGPT (July 2026)

### Summary

This paper develops contour-integral algorithms for computing selected interior singular values of a matrix and generalized singular values of a matrix pair. Although these quantities can be represented as eigenvalues of a Hermitian Jordan--Wielandt matrix or pencil, directly applying FEAST ignores its paired spectral structure and can be sensitive to the initial subspace. The authors analyze four structured spectral-projector choices and construct FEAST-SVD and FEAST-GSVD schemes. Their robust strategy augments the first trial subspace using projectors associated with positive and negative contours, retaining information that a single positive-contour projection may cancel or discard; later iterations revert to the cheaper single-contour update. A Monte Carlo trace estimator approximates the number of values in the requested interval, while Rayleigh--Ritz extraction, residual tests, and soft locking complete the solver. Experiments on twelve SuiteSparse matrices show that the methods typically recover all requested singular or generalized singular values in three or four iterations with high accuracy. The approach also refines low-precision initial solutions and may support spectral slicing or mixed-precision algorithms.

### Contributions

1. Recast partial SVD and GSVD as structured contour-integral eigenproblems on Jordan--Wielandt matrices and pencils.
2. Analyzed four projection strategies and their sensitivity to cancellation and the initial subspace.
3. Introduced a first-iteration two-contour augmentation that improves robustness and accelerates later iterations.
4. Developed FEAST-SVD and FEAST-GSVD algorithms with trace estimation, Rayleigh--Ritz extraction, residual stopping, and soft locking.
5. Demonstrated rapid recovery on twelve sparse test matrices and successful refinement of low-precision starting solutions.
