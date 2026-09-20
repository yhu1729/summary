# 2026CFTB

## ChatGPT (July 2026)

### Summary

Gauss--Newton methods can converge rapidly on PDE-constrained inverse problems, but their Jacobian--vector products normally require additional forward or adjoint PDE solves. This paper proposes gradient-only Gauss--Newton for objectives formed from sums of per-experiment losses. Each loss $\phi_i$ is written as $\rho_i^2/2$, where $\rho_i=\sqrt{2\phi_i}$. The Jacobian row $\nabla\rho_i=\nabla\phi_i/\sqrt{2\phi_i}$ is therefore assembled from function values and gradients already computed for the full objective. Combined with a regularizer Hessian, this gives a low-rank Gauss--Newton approximation without extra PDE solves. Under compact-sublevel, Lipschitz-gradient, uniformly positive regularizer-Hessian, and Wolfe-line-search assumptions, the gradient norm converges to zero. Acoustic full-waveform-inversion tests compare the method with nonlinear conjugate gradient, L-BFGS, and Gauss--Newton CG under equal PDE-solve budgets. It is competitive for uniform acquisition and strongest for realistic uneven receiver coverage. Severe rank deficiency in the approximate Jacobian makes the method approach gradient descent.

### Contributions

1. Reformulated summed PDE-constrained losses so a Gauss--Newton Jacobian can be assembled from per-loss values and gradients.
2. Eliminated sensitivity and adjoint PDE solves beyond those already required for gradient evaluation.
3. Exploited the low-rank structure and regularization through an experiment-space linear system.
4. Proved global convergence to first-order stationarity under the stated regularity and line-search assumptions.
5. Demonstrated competitive full-waveform-inversion performance under fixed PDE-solve budgets and identified rank deficiency as a limiting case.
