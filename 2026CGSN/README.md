# 2026CGSN

## ChatGPT (July 2026)

### Summary

Fusion pilot plants will have little diagnostic port space and harsh operating conditions, motivating confinement-state inference from reactor-compatible microwave diagnostics. Using 260 DIII-D shots with profile-reflectometer data, the authors construct 8,102 time-slice samples and represent each density profile by a cubic spline sampled at ten radial locations concentrated near the plasma edge. A gradient-boosted classifier distinguishes L- from H-mode with 97% mean test accuracy under shot-level train/test splitting. SHAP analysis confirms that edge and pedestal information dominates the prediction. The paper then combines this density-based classifier with an earlier electron-cyclotron-emission temperature classifier. Distances to k-means centers in each diagnostic's training feature space provide confidence weights for a probability ensemble, which reaches 99.2% accuracy across randomized shot splits. A chronological sliding-window test lowers accuracies to 93.1% for reflectometry and 96.0% for the ensemble, showing useful robustness but also distribution drift and a likely need for periodic recalibration.

### Contributions

1. Constructed a fusion-power-plant-relevant H-mode classifier from profile-reflectometer density profiles, including a spline representation that handles incomplete core penetration.
2. Used shot-level rather than snapshot-level splitting to reduce temporal leakage from correlated time slices.
3. Achieved 97% mean test accuracy, with 98% precision, recall, and F1 score, across 100 shot reshuffles.
4. Introduced a confidence-weighted reflectometry and electron-cyclotron-emission ensemble based on distance to training-data clusters, reaching 99.2% accuracy.
5. Quantified chronological distribution drift and identified periodic recalibration as a likely deployment requirement.
