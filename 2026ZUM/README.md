# 2026ZUM

## ChatGPT (July 2026)

### Summary

This paper gives implementable Monte Carlo procedures for loading nine non-Maxwellian velocity distributions into kinetic particle simulations: $(r,q)$, regularized Kappa, subtracted Kappa, finite-width ring and shell, ring and shell Maxwellian, super-Gaussian, and filled-shell distributions. The algorithms reduce sampling to uniform, normal, and gamma variates, supplemented by tailored beta-prime or rejection schemes. Parameter-space tests identify where each method is valid and efficient, and numerical experiments verify sampled densities and moments. A loss-cone filling parameter is incorporated into the subtracted-Kappa recipe. Newly introduced ring and shell Maxwellians have simpler samplers and analytically accessible moments, remain well behaved near zero velocity, and receive a physical interpretation through radial or spherical scattering of a seed population. The paper also identifies GPU limitations caused by divergent rejection loops and missing gamma generators in common vendor libraries.

### Contributions

1. Provided numerical recipes for nine non-Maxwellian plasma velocity distributions.
2. Mapped validity and efficiency regions for beta-prime, post-rejection, and piecewise-rejection samplers.
3. Developed a sampler for the subtracted-Kappa loss-cone model, including partial loss-cone filling.
4. Introduced ring and shell Maxwellians as physically motivated, numerically simpler alternatives to conventional finite-width models.
5. Validated distributions and moments numerically while documenting practical GPU implementation risks.
