# 2026LHKD

## Claude (September 2026)

### Summary

Laser-plasma accelerator beams drift over an operating shift, while the interaction-point conditions responsible are not measured. The authors model operation as a latent state-space system whose hidden state is the normalized laser amplitude $a_0$, normalized plasma density $\tilde n_e$, and residual chirp $C$, estimated shot by shot from centroid energy, energy spread, and charge with an extended Kalman filter. A closed-form emission model, built from relativistic self-focusing, blowout-regime energy scaling, and chirp-dependent downramp injection, maps the state to observables; its Jacobian localizes which variable moved. Separately, hardware-derived transition models linking laser-head temperature, humidity, and room temperature to $a_0$, $C$, and $\tilde n_e$ compete against a random-walk null by predictive likelihood, with profiled coupling gains and a BIC penalty. Two innovation screens and a four-condition gate decide whether to recommend an intervention. In synthetic sessions generated from the same model family, the responsible mechanism family is recovered whenever its energy signature is visible, humidity drift is unidentifiable because $\partial E/\partial C=0$ at the operating point, and attribution is limited by environmental excitation rather than session length. The authors stress that the emission model bounds the achievable accuracy and that validation on measured data remains open.

### Contributions

1. Formulated laser-plasma accelerator operation as a three-variable physical latent state-space model whose separate emission and transition models split drift diagnosis into localization and attribution.
2. Constructed a differentiable reduced-physics emission map in which chirp enters energy spread and charge at first order, making compressor drift distinguishable from laser-energy and gas-density drift.
3. Made the candidate transition models memoryless so that each score is an exact log marginal likelihood, and derived a family-margin evidence measure growing with shot count and with the squared difference of mechanism energy signatures.
4. Designed a lag-1 autocorrelation and normalized-innovation-squared screen that lowered the session-level false-alarm rate under a correct null from 85.0% to 0.01%, feeding a gate that issues falsifiable recovery predictions.
5. Showed that deliberate 6 °C laser-head dithering yields decisive attribution that ambient drift never provides, that margins stay decisive up to twice the baseline observation noise, and that the full causal candidate excludes the null without identifying a subsystem.
