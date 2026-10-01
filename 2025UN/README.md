# 2025UN

## ChatGPT (July 2026)

### Summary

This paper introduces nonlinear Gaussian process tomography for plasma diagnostics when the reconstructed physical quantity must be non-negative. Instead of enforcing positivity through sampling-based posteriors in earlier Gaussian process tomography, the method uses a logarithmic Gaussian process and applies a Laplace approximation. This makes the constraint natural while keeping inference faster than fully sampling-based alternatives. The authors demonstrate the method on optical-diagnostic tomography for the Ring Trap 1 device, where emissivity is the constrained positive quantity. In that case study, the logarithmic Gaussian process reconstruction is more accurate than standard Gaussian process tomography and minimum Fisher information reconstruction. The work therefore frames positivity not as an after-the-fact correction, but as part of the statistical model used for the inverse problem. Its main technical value is a practical constrained Bayesian reconstruction method for diagnostics where negative inferred densities, emissivities, or related quantities are physically meaningless.

### Contributions

1. Formulated nonlinear Gaussian process tomography for positive-valued plasma diagnostic quantities.
2. Used a logarithmic Gaussian process to encode non-negativity directly in the reconstruction model.
3. Applied a Laplace approximation to reduce the cost relative to sampling-based constrained posteriors.
4. Demonstrated the method on Ring Trap 1 optical-diagnostic tomography.
5. Showed improved reconstruction accuracy against standard Gaussian process tomography and minimum Fisher information methods.
