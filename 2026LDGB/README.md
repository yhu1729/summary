# 2026LDGB

## ChatGPT (September 2026)

### Summary

QuaSSis is a two-dimensional, three-velocity-component quasistatic particle-in-cell code for dilute ultrarelativistic beams propagating through denser plasmas. It separates slow beam evolution from the rapid plasma response and extends this approach to the oblique two-stream instability. A finite-difference boundary scheme supports transversely periodic systems by evolving boundary field values before solving the interior equations. Benchmarks with Gaussian electron beams and transversely uniform electron–positron beams reproduce CALDER simulations of density modulation, field spectra, instability growth, and saturation. The reported comparisons reduce computational consumption from thousands of core-hours to a few core-hours, rather than demonstrating equivalent wall-clock speedups. Regularly spaced macroparticles with randomized weights allow the initial instability seed to be adjusted without increasing particle count. Analytical density- and current-noise estimates explain this control and identify a floor imposed by finite transverse momentum spread. Lower initial noise delays saturation without changing its level in the tested cases. Validation concerns the oblique-instability regime with effectively immobile background ions; it does not establish accuracy for arbitrary beam-plasma dynamics.

### Contributions

1. Demonstrated quasistatic modeling of the oblique two-stream instability with QuaSSis, including finite-temperature plasma equations and separate beam and plasma advances.
2. Detailed a finite-difference treatment of transverse periodic boundaries that resolves the otherwise undetermined boundary values of the quasistatic Poisson problems.
3. Reproduced full-PIC beam structures, spectra, growth, and saturation for Gaussian and transversely uniform beams, while reducing the reported core-hour costs by roughly three orders of magnitude.
4. Introduced ordered macroparticle positions with randomized weights to control instability seeding at fixed particle count and computational cost.
5. Derived noise scalings for multiple particle shape orders and dimensions, explaining both delayed saturation at lower noise and the limiting contribution of transverse momentum fluctuations.
