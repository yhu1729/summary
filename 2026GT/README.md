# 2026GT

## ChatGPT (July 2026)

### Summary

Many global solvers for multivariate polynomial systems replace the original problem with univariate rootfinding or generalized eigenvalue subproblems. The paper shows that popular algebraic constructions can make these intermediate problems exponentially worse conditioned as the number of variables grows, even when the target root is comparatively well conditioned. It treats Gröbner-basis elimination, rational univariate representations, multiparameter eigenproblems solved by operator determinants, normal-form multiplication matrices, and Macaulay resultants, extending earlier analyses of hidden-variable resultants. Explicit polynomial systems quantify the condition-number amplification and show that changing polynomial bases or variable order does not remove several of the failures. New formulas connect operator-determinant conditioning to the original Jacobian and singular values of determinantal representations, and connect multiplication-matrix and Macaulay conditioning to Lagrange interpolants represented through a determinant. Numerical experiments reproduce the predicted loss of accuracy for bivariate and higher-dimensional examples. The results diagnose instability in common algorithmic variants rather than prove that every possible algebraic formulation is unstable: unusually chosen projections, bases, or determinantal representations remain potential escape routes, and homotopy-continuation methods are outside the analysis.

### Contributions

1. Unified the stability analysis of major algebraic multidimensional rootfinders by comparing each constructed subproblem with the conditioning of the original root.
2. Constructed polynomial systems for which Gröbner elimination and bounded linear rational-univariate projections incur condition-number growth exponential in dimension.
3. Derived a condition-number formula for operator-determinant generalized eigenproblems and used it to expose exponential amplification in standard multiparameter formulations.
4. Characterized multiplication-matrix and Macaulay-resultant conditioning through Jacobians and Lagrange interpolants, yielding new exponential-instability examples.
5. Confirmed the theoretical scaling in numerical experiments while identifying the precise assumptions and possible routes around each instability mechanism.
