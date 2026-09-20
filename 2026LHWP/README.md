# 2026LHWP

## ChatGPT (July 2026)

### Summary

This paper introduces a time-embedded convolutional neural network (TCNN) for one-dimensional nonlocal electron heat transport in plasmas. Trained on fully kinetic OSIRIS particle-in-cell simulations, the model jointly predicts normalized heat flux and the nonlocality measure $\lambda_{\mathrm{free}}/L_T$. Time-indexed convolutions represent evolving transport rather than imposing the quasistationary kernel assumed by the Luciani--Mora--Virmont model and the authors' earlier LINN surrogate. Across collisionalities, TCNN most clearly improves predictions in strongly nonlocal, rapidly evolving regimes; local quasistatic cases remain better suited to a possible TCNN--LINN hybrid. Architecture variants show that convolutional depth and latent spatial projection materially improve nonlocal predictions. Tests with perturbed inputs show sublinear error growth as noise increases. The current isobaric one-dimensional training data and expensive multidimensional kinetic data limit immediate deployment, but the architecture provides a stable, physically structured surrogate for future radiation-hydrodynamics coupling.

### Contributions

1. Designed a time-embedded convolutional architecture for dynamic nonlocal plasma heat transport.
2. Jointly predicted heat flux and a physically coupled nonlocality parameter.
3. Trained and tested the surrogate on fully kinetic particle-in-cell simulations across collisional regimes.
4. Used architecture variants to isolate the roles of convolutional depth and latent spatial projection.
5. Demonstrated robustness to noisy inputs and clarified extensions toward multidimensional transport models.
