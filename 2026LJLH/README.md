# 2026LJLH

## ChatGPT (July 2026)

### Summary

FourierSpecNet is a learned Boltzmann collision operator whose architecture mirrors the separable convolution structure of a fast Fourier spectral solver. Learnable coefficients occupy a fixed truncated Fourier band, so the parameter count does not grow with velocity-grid resolution and one trained model can evaluate unseen grids. Training targets are spectral collision operators for Gaussians, Gaussian mixtures, and perturbed Gaussians. A consistency result bounds learned-operator error by approximation and spectral-truncation terms and gives convergence as bandwidth and discretization are refined under kernel-mode decay assumptions. Experiments cover Maxwellian, hard-sphere, inelastic, and three-dimensional velocity cases. Predictions track analytic or spectral references, approximately preserve physical moments, and retain similar errors across tested resolutions. At large grids, repeated inference is substantially faster than the reference fast spectral implementation, excluding training cost.

### Contributions

1. Designed a neural architecture that reproduces the separable convolution structure of a fast spectral collision operator.
2. Made the learned parameters independent of grid resolution, enabling zero-shot super-resolution.
3. Proved a consistency result relating learned-operator error to coefficient approximation and spectral truncation.
4. Validated the method for elastic, inelastic, and three-dimensional velocity-space problems.
5. Demonstrated approximate physical-moment preservation and up to roughly $72\times$ inference speedup at the largest tested grid.
