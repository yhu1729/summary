# 2026H

## ChatGPT (July 2026)

### Summary

This paper adapts one-step Drifting Models to molecular conformations and uses force labels to shift generation from biased training data toward the Boltzmann distribution. For Gaussian kernels, a Drifting Score Identity expresses attraction as a kernel-weighted score average; the force--score relation then gives a Boltzmann force identity. Force-Interpolated Drifting blends Cartesian displacements with force directions, while Force-Aligned Kernel changes neighbor weights. On a biased 3,000-frame MD17 ethanol subset, force interpolation works best in Cartesian coordinates, whereas kernel reweighting works best in pairwise-distance space because it preserves realizable molecular geometry. The latter reaches distance-histogram total-variation distance $0.089$, bond mean absolute error $0.006\,\text{\AA}$, and 100% bond stability. Generation is one-step and millisecond-scale. The title's million-fold acceleration is an extrapolation across reported baselines and hardware rather than a direct same-hardware benchmark.

### Contributions

1. Established Drifting Score and Drifting Force identities connecting data attraction, score functions, and molecular forces.
2. Introduced force-interpolated and force-aligned-kernel guidance mechanisms.
3. Showed how force guidance moves the drifting equilibrium toward, though not generally exactly to, the Boltzmann distribution.
4. Identified a representation-dependent reversal in which guidance mechanism performs best.
5. Achieved low distributional error and perfect tested bond stability on the biased MD17 ethanol experiment.
