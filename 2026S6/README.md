# 2026S6

## ChatGPT (July 2026)

### Summary

This paper constructs a transparent boundary condition for two-dimensional exterior Helmholtz problems with compactly supported forcing. The exterior solution is represented by the method of fundamental solutions on concentric source and collocation circles. Equally spaced points make the discrete Dirichlet-to-Neumann map circulant, so it is diagonalized and applied efficiently with the discrete Fourier transform. Coupling this map to a finite-element formulation truncates the unbounded domain without replacing the inhomogeneous equation by a boundary-integral volume treatment. Numerical tests separately examine high-wavenumber map accuracy and the complete finite-element solution for circular and irregular interior boundaries. They show high accuracy when the source circle is chosen appropriately and confirm that the resulting transparent condition reproduces manufactured exterior solutions. The analysis also relates the circulant discretization to the Fourier eigenfunctions of the continuous map. Extension to three dimensions is plausible through block-circulant structure, while convergence of the discrete operator in a suitable topology remains open.

### Contributions

1. Constructed a method-of-fundamental-solutions discretization of the exterior Helmholtz Dirichlet-to-Neumann map.
2. Exploited concentric circular point sets to obtain a circulant map with FFT-based application.
3. Embedded the discrete map as a transparent boundary condition in a finite-element formulation.
4. Treated compactly supported inhomogeneous forcing on unbounded exterior domains without domain meshing at infinity.
5. Verified high-wavenumber map accuracy and complete solutions on circular and irregular geometries.
