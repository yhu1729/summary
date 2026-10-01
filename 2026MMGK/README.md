# 2026MMGK

## Claude (September 2026)

### Summary

Accurate particle-in-cell (PIC) modeling of high-intensity laser–plasma interaction requires the laser's field amplitude and phase, but experiments often provide only fluence images at a few transverse planes. The authors present a cylindrical implementation of the Gerchberg–Saxton algorithm with mode decomposition (GSA-MD), which iteratively fits complex Laguerre–Gauss mode coefficients to the fluence images on per-plane polar grids, and describe it together with the earlier Cartesian Hermite–Gauss version in one framework. On averaged fluence images from the DRACO laser at HZDR, which are highly rotationally symmetric, 105 Laguerre–Gauss modes reached a reconstruction error of about 3.4% in roughly 75 s, whereas 25 Hermite–Gauss modes in similar time gave an error 3.8 times larger and far larger beam-width errors. Sampling the azimuth at 36 rather than 720 points kept comparable accuracy and cut the time to 5 s. Analytical expressions map each Laguerre–Gauss mode onto azimuthal Fourier harmonics for laser injection in the PIC code SMILEI; a vacuum-propagation run reproduces the reconstructed fluence within 3.4%. In an ionization-injection wakefield simulation, the reconstructed laser yields a broad electron spectrum with more charge than a Gaussian fit (214 versus 150 pC). The efficiency gain applies to nearly symmetric lasers; codes and data are released.

### Contributions

1. Implemented a Laguerre–Gauss, cylindrical-grid version of the Gerchberg–Saxton algorithm with mode decomposition, unified with the Hermite–Gauss Cartesian version.
2. Showed by benchmark that the cylindrical version reconstructs nearly symmetric lasers more accurately at equal cost, and that Nyquist-guided coarse azimuthal sampling gives preliminary reconstructions in seconds on a laptop.
3. Derived closed-form mappings from Laguerre–Gauss coefficients to the azimuthal harmonics of the injected laser field, including rescaling to a prescribed energy and temporal profile.
4. Demonstrated reconstructed-laser PIC simulations whose wakefield results contradict the previously reported trend of lower charge and energy for realistic lasers, arguing that realistic laser models are needed to design working points.
5. Defined a rotational symmetry parameter for comparing laser fluence symmetry and a separable storage of mode fields that greatly reduces memory use.
