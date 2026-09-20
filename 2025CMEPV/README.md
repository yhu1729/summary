# 2025CMEPV

## ChatGPT (July 2026)

### Summary

Hypoxia-activated prodrugs target oxygen-poor tumor regions, but their activation, transport, metabolism, and cytotoxicity are strongly coupled. This work builds a mixed-dimensional model for tirapazamine that combines three-dimensional tissue transport, one-dimensional blood flow in a synthetic capillary network, and a zero-dimensional pharmacokinetic/pharmacodynamic surrogate. The framework represents vascular delivery, oxygen diffusion and consumption, drug exchange and metabolism, and cell survival. One-way coupling from the reduced nonlinear surrogate to the spatial finite-element model avoids solving cellular-scale kinetics throughout the tissue. A two-stage Morris global sensitivity analysis first screens parameters with the inexpensive surrogate, then studies seven influential parameters in the 3D--1D--0D model. Vascular drug concentration dominates tissue exposure, while drug metabolism and oxygen-related parameters strongly influence survival. The spatial model preserves similar importance rankings but reveals larger interaction effects and heterogeneous drug and survival distributions tied to vascular density. Signed sensitivities also show that oxygen transport can affect survival non-monotonically through competing activation and accumulation mechanisms. The results are exploratory: they use one synthetic network, quasi-steady oxygen transport, and no calibration to experimental or patient data, so the model generates hypotheses rather than clinical predictions.

### Contributions

1. Formulated a mixed-dimensional 3D--1D model coupling tissue transport to blood flow in an embedded microvascular network.
2. Integrated oxygen-dependent tirapazamine metabolism and cell survival through a reduced pharmacokinetic/pharmacodynamic model.
3. Reduced the global nonlinear cost through one-way coupling of the 0D surrogate to the spatial finite-element model.
4. Designed a two-stage Morris analysis that screens parameters cheaply before evaluating a reduced set in the multiscale model.
5. Identified vascular drug concentration, oxygen availability, and metabolic rates as dominant drivers while exposing spatial heterogeneity and nonlinear interactions.
