# 2026SG

## ChatGPT (July 2026)

### Summary

This paper formulates a direct sampling method for locating time-dependent electromagnetic sources from sparse, multi-frequency far-field measurements. A temporal Fourier transform converts Maxwell's equations into frequency-domain systems with frequency-dependent sources, while suitable polarization vectors reduce the vector data to scalar indicators. For an impulsive source, combining measurements from two opposite observation directions identifies the unknown excitation time. Once that time is known, data from one direction recover the smallest slab between parallel hyperplanes containing the source support; intersecting slabs from several sparse directions approximates its $\Theta$-convex hull. The construction also treats sources radiating over a finite interval when either the starting or ending time is known. The indicators require neither iterative forward solves nor a divergence-free source assumption. Three-dimensional synthetic experiments recover excitation times, shifted slabs, and multiple source geometries. Frequency integration provides substantial noise tolerance: the principal slab remains visible in the reported tests even with 80% multiplicative noise, although its boundary becomes more oscillatory.

### Contributions

1. Extended direct sampling to frequency-dependent electromagnetic inverse sources governed by Maxwell's equations.
2. Constructed opposite-direction indicators that recover an impulsive source's excitation time.
3. Recovered directional support slabs and their multi-direction $\Theta$-convex-hull intersection.
4. Extended the reconstruction to finite radiation intervals with one known temporal endpoint.
5. Demonstrated three-dimensional reconstruction without divergence-free assumptions and under high synthetic noise.
