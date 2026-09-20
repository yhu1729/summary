# 2025VCCC

## ChatGPT (July 2026)

### Summary

The paper constructs projection-based reduced-order models for finite-element Lagrangian hydrodynamics and hyper-reduces their nonlinear force evaluations with the empirical quadrature procedure (EQP). Proper-orthogonal-decomposition bases reduce position, velocity, and internal-energy states, while time windowing limits basis growth in advection-dominated flows. The central contribution is a conservative EQP variant that enriches the energy basis with the constant-energy mode and uses one shared reduced quadrature rule for velocity and energy forces. These conditions preserve the pressure-work cancellation underlying discrete total-energy conservation. Implementations in Laghos and libROM are tested on Sedov blast, Gresho vortex, triple-point, and Taylor--Green vortex benchmarks. Conservative EQP maintains accuracy and useful speedups comparable to basic EQP while reducing total-energy drift to approximately $10^{-13}$--$10^{-14}$. The experiments reproduce training trajectories rather than testing out-of-sample prediction.

### Contributions

1. Derived two projection-based reduced formulations from a high-order finite-element Lagrangian Euler discretization.
2. Applied EQP to replace full nonlinear spatial integration with sparse, nonnegative reduced quadrature rules.
3. Established sufficient conditions for strong discrete total-energy conservation in the hyper-reduced RK2A model.
4. Realized those conditions through zero offsets, energy-basis enrichment, and a coupled velocity--energy quadrature rule.
5. Validated near-machine-precision energy conservation on four two- and three-dimensional hydrodynamics benchmarks.
