# 2026HS2

## ChatGPT (July 2026)

### Summary

This paper recasts function extrapolation as projection onto a certified feasible set. An anchor is an auxiliary function with a bound on its distance from the unknown target over the extrapolation domain $\Xi$; one or more anchor balls therefore constrain admissible predictions directly where data are absent. Projecting any baseline predictor onto such a set is proved not to increase its $\Xi$-error and to improve it strictly when the predictor lies outside the set, with quantitative improvement bounds. To construct certificates from in-domain error, the authors derive a tight spectral amplification constant from the largest eigenvalue of a $\Xi$-Gram matrix and a more numerically robust inner-domain bound. They also model error directions probabilistically to obtain less conservative, confidence-controlled radii. Polynomial, geomagnetic-field, spherical-harmonic, and nonlinear-oscillator experiments illustrate the guarantees and often reduce extrapolation error. The guarantees remain conditional on valid anchor radii; probabilistic certificates additionally depend on the assumed directional error model.

### Contributions

1. Formulated model-independent extrapolation as projection onto intersections of anchor-defined feasible balls over $\Xi$.
2. Proved non-worsening and strict-improvement results, including explicit bounds based on the predictor's distance from a feasible ball.
3. Derived a Rayleigh--Ritz-tight spectral condition number relating in-domain and extrapolation errors.
4. Developed an inner-domain certificate for improved numerical robustness and probabilistic radii with prescribed confidence.
5. Tested simple and data-derived anchors across synthetic, geomagnetic, manifold, and differential-equation examples.
