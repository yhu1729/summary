# 2026KDBK

## ChatGPT (July 2026)

### Summary

This study replaces expensive particle-in-cell scans of a laser-plasma injector with machine-learning surrogate models for rapid design and optimization. Using more than 3,000 simulations spanning laser and plasma-target parameters, the authors compare multilayer perceptrons, decision-tree models, and Gaussian processes for predicting electron-beam energy, charge, energy spread, and emittance. A compact multilayer perceptron trained on a 500-simulation random scan achieved $R^2=0.93$ and evaluated configurations roughly $10^7$ times faster than particle-in-cell simulation. The resulting surrogate supports random search, Bayesian optimization, and multi-objective Bayesian optimization, enabling the discovery of target working points and stable operating regions that would be impractical to map directly. The analysis also emphasizes a central limitation: predictions degrade where training samples are sparse and at the low end of several beam outputs. Uniform coverage and targeted additional simulations are therefore important for reliable design. The models can be updated with new simulation or experimental data and could serve as fast electron-source components in start-to-end accelerator studies and feedback-control systems.

### Contributions

1. Built laser-plasma-injector surrogates from a large particle-in-cell simulation data set.
2. Compared multilayer perceptron, decision-tree, and Gaussian-process models across four beam-quality outputs.
3. Achieved $R^2=0.93$ with a compact model trained on 500 simulations and approximately $10^7$-fold faster evaluation.
4. Used surrogates with single- and multi-objective optimization to locate target working points and stability regions.
5. Quantified the dependence of predictive reliability on training-data coverage and identified sparse-region limitations.
