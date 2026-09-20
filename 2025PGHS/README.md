# 2025PGHS

## ChatGPT (July 2026)

### Summary

Nonlinear gyrokinetic simulations resolve plasma turbulence in a five-dimensional phase space but are too costly for repeated transport predictions, while quasilinear reductions omit mode coupling and zonal flows. GyroSwin is a neural surrogate trained directly on nonlinear 5D distribution functions from the GKW code under an adiabatic-electron approximation. It extends shifted-window hierarchical transformers to five dimensions, couples 5D distributions with 3D electrostatic potentials through latent cross-attention and integration layers, and separates spectral channels to encode the special role of zonal modes. Multitask training predicts the evolving distribution, potential, and heat flux together. Tests on in-distribution and out-of-distribution simulations show more stable autoregressive rollouts and lower time-averaged heat-flux error than quasilinear models and alternative neural surrogates. The model also reproduces flux and turbulence spectra and captures zonal-flow profiles, providing diagnostics unavailable from scalar regressors. Scaling experiments use 241 simulations, about 6 TB of data, and models up to one billion parameters; inference is roughly three orders of magnitude faster than GKW. Current limitations include accumulated rollout error, omission of the linear growth phase, one electron approximation, and sparse coverage of the four-dimensional operating-parameter space.

### Contributions

1. Introduced a scalable neural surrogate that autoregressively evolves the full 5D gyrokinetic distribution rather than only scalar transport outputs.
2. Extended hierarchical shifted-window attention, patch operations, and conditioning mechanisms to five-dimensional fields.
3. Developed latent cross-attention and integration modules that couple 5D distributions, 3D potentials, and scalar heat fluxes.
4. Added physics-motivated channelwise mode separation and demonstrated recovery of nonlinear spectra and zonal flows.
5. Demonstrated improved heat-flux prediction, stable rollouts beyond 100 steps, billion-parameter scaling, and roughly thousand-fold faster inference than GKW.
