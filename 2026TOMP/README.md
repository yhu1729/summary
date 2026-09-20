# 2026TOMP

## ChatGPT (July 2026)

### Summary

This paper verifies the ssV code, a semi-Lagrangian Vlasov solver for a hybrid kinetic-gyrokinetic plasma model with fully kinetic ions and drift- or gyrokinetic electrons. The model is intended for weakly magnetized and multiscale regimes where fluid, standard hybrid, or fully gyrokinetic approximations miss important ion-scale and electron-response physics. The authors derive the coupled field formulation, discuss the Ampere cancellation issue, and compare several advection schemes, including PFC, FCV, FCV-Umeda, and SLMP5. Benchmarks cover linear and nonlinear Landau damping, ion-acoustic waves, ion Bernstein waves, and kinetic Alfven waves. The tests show agreement with analytic predictions and previous results, with SLMP5 giving the best balance of accuracy, monotonicity, and numerical stability. The implementation provides a practical reduced kinetic route for space and laboratory plasma studies, while future work targets 3D3V/3D1V extensions and GPU acceleration.

### Contributions

1. Presented a hybrid kinetic-gyrokinetic formulation coupling fully kinetic ions to reduced electron dynamics.
2. Implemented the model in ssV with high-order semi-Lagrangian transport options.
3. Compared PFC, FCV, FCV-Umeda, and SLMP5 on smooth and nonsmooth Vlasov benchmarks.
4. Verified Landau damping, ion-acoustic, ion Bernstein, and kinetic Alfven wave behavior against theory.
5. Identified SLMP5 as the most robust tested scheme for accurate, stable reduced kinetic plasma simulations.
