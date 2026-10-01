# 2026SP

## Claude (September 2026)

### Summary

The authors analyse two-dimensional incompressible flow past two side-by-side square cylinders at Reynolds number 200 with a gap equal to the cylinder side, where a flapping gap jet disrupts vortex shedding. Finite-volume simulations and spectral proper orthogonal decomposition (SPOD) identify three frequency bands: jet flapping ($St\approx0.063$), vortex shedding ($St\approx0.168$), and a subharmonic linked to downstream vortex merging. Linearising the Navier–Stokes equations about the chaotic trajectory, restricted to two-dimensional perturbations, they compute six Lyapunov exponents and the corresponding covariant Lyapunov vectors (CLVs), the generally non-orthogonal directions of asymptotic growth and decay. The flow has two positive exponents, the largest about 0.1. The leading CLV is concentrated in the near wake and, through SPOD, carries the flapping and shedding frequencies; the second peaks farther downstream and captures the subharmonic merging instability. Angles between CLVs show that hyperbolicity is violated mainly by near-tangency of neutral and stable directions, in up to 2.4% of samples. Global linear stability analysis of the time-averaged flow yields a neutral mode matching the leading CLV's shedding structure and frequency but misses the growth of that direction, jet flapping, and the subharmonic. A Reynolds-number sweep shows the Lyapunov spectrum marking the transitions to periodic, chaotic, and flip-flop regimes.

### Contributions

1. Computed Lyapunov exponents and covariant Lyapunov vectors for a chaotic two-cylinder wake, finding two unstable directions with footprints in the near wake and farther downstream and the most stable computed direction active near the outlet.
2. Applied SPOD to covariant Lyapunov vectors, which the authors describe as the first such use, linking the leading vector to jet flapping and shedding and the second to subharmonic vortex pairing.
3. Assessed hyperbolicity from the statistics of angles between vectors, finding violations concentrated in the neutral and stable subspaces and near-orthogonality for vectors with non-overlapping footprints.
4. Compared Lyapunov and mean-flow global stability analyses explicitly for a chaotic flow, showing that the mean-flow analysis labels as neutral a direction that is unstable.
5. Used the three leading exponents to identify transitions at $Re\approx67$ (periodic), $85$ (chaotic), and $125$ (flip-flop, second positive exponent), and released open-source code for the exponent and vector computations.
