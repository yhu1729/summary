# 2026HHLZ

## ChatGPT (July 2026)

### Summary

Deep Picard Iteration solves high-dimensional semilinear and fully nonlinear parabolic PDEs by converting each Picard step into supervised regression for solution values and gradients. Feynman--Kac sampling supplies value labels and Bismut--Elworthy--Li formulas supply gradient labels. The authors prove that naive Malliavin-weight gradient estimators have infinite variance and remove their singular components with control variates, yielding finite-variance training targets. Warm-started neural networks then regress the updated functions, with data generation separable across samples. On 100-dimensional Burgers-type, Hamilton--Jacobi--Bellman, and fully nonlinear equations, the method is more accurate and less sensitive to the gradient-loss weight than the tested PINN, Deep BSDE, diffusion-DBSDE, and DBDP baselines, especially for stronger nonlinearities and longer horizons. A ten-dimensional reverse-SDE example recovers a multimodal target distribution, while the corresponding 100-dimensional gradient remains insufficient for accurate sampling. Experiments use synthetic problems with known solutions on one GPU; convergence conditions for fully nonlinear Picard iteration, boundary handling, training-distribution design, and demonstrated parallel scaling remain open.

### Contributions

1. Recast nonlinear high-dimensional PDE solution as sequential value-and-gradient regression.
2. Combined Feynman--Kac and Bismut--Elworthy--Li labels in a practical neural method.
3. Proved infinite variance of naive gradient estimators and derived finite-variance controls.
4. Improved accuracy and hyperparameter robustness across several 100-dimensional benchmarks.
5. Demonstrated modest gradient-label overhead and embarrassingly parallel data generation.
