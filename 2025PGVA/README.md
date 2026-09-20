# 2025PGVA

## ChatGPT (July 2026)

### Summary

This living report develops a reproducible benchmark for constructing multivariate surrogate models from sampled tensors. Fifty functions spanning two to ten variables, polynomial, rational, and non-rational structure, smooth and nonsmooth behavior, and tensors from kilobytes to hundreds of megabytes are evaluated with seven implementations: direct and adaptive multivariate Loewner methods, MDSPACK, Kolmogorov--Arnold networks, parametric AAA variants, and a multilayer perceptron. Models are compared using out-of-sample root-mean-square error, construction time, surrogate complexity, convergence, tuning sensitivity, and usability. The report also derives the multivariate Loewner Framework's tensor-product barycentric representation, explains recursive null-space construction and variable decoupling, and supplies a MATLAB tutorial. Across the benchmark, Loewner-based methods recover polynomial and rational functions accurately and scale to tensors near one gigabyte, whereas several alternatives encounter memory or runtime limits as dimensionality grows. Non-rational cases favor adaptive methods but expose problem-dependent tuning. The study emphasizes diagnostic comparison rather than a universal ranking and releases code to reproduce and extend the results.

### Contributions

1. Curated 50 multivariate test functions varying in dimension, algebraic structure, regularity, symmetry, and tensor size.
2. Defined a common protocol measuring out-of-sample accuracy, construction time, model complexity, convergence, tuning sensitivity, and usability.
3. Consolidated the multivariate Loewner Framework, including tensor barycentric forms, recursive null-space construction, and a MATLAB tutorial.
4. Benchmarked seven rational-approximation and neural-network implementations across the complete test collection.
5. Released reproducible code and identified parameter selection, approximation-order choice, and memory limits as concrete open problems.
