# 2026NO

## ChatGPT (July 2026)

### Summary

The authors study mixed-precision iterative refinement for linear discrete inverse problems, where ill-conditioning and noisy data make an unregularized least-squares solution unstable. They apply refinement to standard Tikhonov regularization and express its iterates recursively through a preconditioned Landweber method with a Tikhonov-type preconditioner. This representation shows that refinement acts as a spectral filter rather than merely correcting a conventional linear solve. The algorithm permits different precisions for the regularized factorization/preconditioner, working updates, and residual evaluation, allowing costly operations to use lower precision while preserving higher precision where error sensitivity is greatest. MATLAB experiments simulate multiple precision triples on test inverse problems, including spectral reconstruction and image deblurring. Across the reported cases, mixed-precision refinement generally reaches stable relative reconstruction errors within a few decimal places of all-double-precision results and outperforms the paper's approximate iterative-refinement benchmark. Lower-precision preconditioners can increase run-to-run variability, especially with weak regularization; stronger regularization reduces that variability but may increase reconstruction error. The results support mixed precision for regularized inverse problems while showing that precision choices and regularization strength must be selected together.

### Contributions

1. Formulated mixed-precision iterative refinement directly for Tikhonov-regularized inverse problems.
2. Derived a recursive filtered-solution interpretation using preconditioned Landweber iteration.
3. Separated preconditioner, working, and residual arithmetic into independently chosen precisions.
4. Demonstrated reconstruction accuracy within a few decimal places of double precision in the tested problems.
5. Quantified how low-precision preconditioning and regularization jointly affect solution variability and error.
