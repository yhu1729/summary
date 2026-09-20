# 2025HYSB

## ChatGPT (July 2026)

### Summary

Meshfree collocation methods approximate differential operators directly on irregular point clouds, but overlapping terminology and independently developed derivations obscure how the methods relate. This overview traces their development from scattered-data interpolation and generalized finite differences through moving least squares, reproducing kernels, radial basis functions, and related particle methods. It formulates their strong-form discrete operators in common vector and matrix notation, then classifies reviewed methods by whether they arise from moment approximation, minimization of approximation error, or minimization of stencil weights. The framework reveals cases that are mathematically identical despite different names and isolates consequential distinctions, including treatment of the zeroth moment, symmetry of the moment matrix, allowable basis functions, and added penalty terms. Those choices can affect computational cost, explicit-time stability, wavenumber dissipation, boundary treatment, and noise robustness. The authors also derive a generalized $\ell^2$ weight-minimization principle that permits arbitrary anisotropic basis functions and asymmetric moment matrices. It recovers the same discrete operator as moment cancellation, creating a formal bridge between two derivational families and potentially allowing theory to transfer between them. A tabulated classification and supplementary encyclopedia consolidate the surveyed methods, while application-specific method selection and detailed numerical comparisons remain outside the review's scope.

### Contributions

1. Reconstructed the historical development of meshfree collocation across communities whose differing terminology led to parallel derivations and rediscoveries.
2. Expressed the reviewed methods within one strong-form operator framework using consistent vector and matrix notation.
3. Classified methods by their derivational principle and supplied a consolidated table and supplementary encyclopedia of their operators, bases, and moment treatments.
4. Identified exact equivalences and technically important differences involving zeroth moments, matrix symmetry, basis restrictions, and penalty terms.
5. Introduced generalized $\ell^2$ weight minimization and proved that it reproduces the moment-approximation operator while allowing arbitrary anisotropic basis functions.
