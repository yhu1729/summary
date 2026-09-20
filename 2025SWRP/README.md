# 2025SWRP

## ChatGPT (July 2026)

### Summary

Thermal radiation transport spans rapidly changing physical timescales, from photon streaming in optically thin regions to slow diffusion in optically thick material, making fixed timesteps inefficient or inaccurate. This work develops adaptive time integration for deterministic gray and multifrequency transport using a high-order--low-order moment representation. It extends a semi-implicit-explicit formulation to multifrequency problems and introduces a higher-order semi-implicit variant that treats every component except opacity implicitly. Four second-order, asymptotic-preserving implicit-explicit Runge--Kutta schemes receive newly derived embedded methods for local error estimation. Because storing embedded angular and frequency-dependent intensities would be expensive, timestep control uses only material temperature or radiation energy, adding negligible storage and computational overhead. Gray two-dimensional tophat and multifrequency one-dimensional Larsen tests show timesteps varying naturally over four to five orders of magnitude as radiation enters new materials or navigates geometric corners. Radiation-energy estimates generally demand smaller steps and improve accuracy relative to temperature-based estimates. In fixed-step multifrequency tests, the implicit-explicit formulation exhibits order reduction, whereas the semi-implicit formulation recovers the intended convergence behavior and errors two to three orders of magnitude smaller. The study is limited to standalone transport; coupling to radiation hydrodynamics remains future work.

### Contributions

1. Extended moment-based semi-implicit-explicit integration from gray to multifrequency thermal radiation transport.
2. Introduced a higher-order semi-implicit formulation that resolves all components implicitly except temperature-dependent opacity.
3. Derived embedded error estimators for four robust, asymptotic-preserving implicit-explicit Runge--Kutta schemes.
4. Reduced adaptive-step overhead by estimating temporal error solely from low-dimensional temperature or radiation-energy moments.
5. Demonstrated four-to-five-order timestep variation on tophat and Larsen benchmarks and quantified the accuracy trade-offs between estimators and integration formulations.
