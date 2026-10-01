# 2026ZL

## ChatGPT (July 2026)

### Summary

Seven solvers for the generalized probability density evolution equation are compared within a common probability-density-evolution framework. The study evaluates finite-difference, finite-volume, and discontinuous-Galerkin grid methods; radial-basis-function and reproducing-kernel-particle meshfree collocation; and physics-informed neural networks with multilayer-perceptron and Kolmogorov--Arnold architectures. Analytical Euler--Bernoulli beam and nonlinear Kirchhoff-plate examples expose how independent probability sampling and response-space discretization cause grid sensitivity. Meshfree methods reduce that sensitivity and numerical dispersion for pure density evolution, whereas grid methods naturally support upwind absorbing boundaries for time-dependent reliability; finite-volume WENO gives the smallest reported reliability error. The neural solvers are flexible but require separate training per sample and run one to two orders of magnitude slower than classical methods. The work extends the framework to residual probability under absorbing failure boundaries, but evaluates only two systems and one failure threshold. Meshfree and neural methods still lack an intrinsic treatment of asymmetric absorbing boundaries, optimal grid density is not known in advance, and the two principal error sources are not separated a posteriori.

### Contributions

1. Benchmarked seven grid, meshfree, and neural GDEE solvers against analytical solutions.
2. Diagnosed probability-sampling and response-grid imbalance as the source of grid sensitivity.
3. Established meshfree advantages for low-dispersion probability-density evolution.
4. Extended the framework to time-dependent reliability with absorbing boundaries.
5. Quantified finite-volume reliability accuracy and the large neural-network runtime penalty.
