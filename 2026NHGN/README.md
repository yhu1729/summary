# 2026NHGN

## ChatGPT (July 2026)

### Summary

PanoMHD is a self-supervised multimodal dynamics model that predicts both global tokamak performance and high-dimensional Mirnov-coil magnetic-fluctuation spectrograms from recent plasma states and control commands. A VQ-VAE discretizes cross-power and cross-phase spectrograms, scalar signals are quantized, and a causal decoder-only Transformer predicts the next $50\,\mathrm{ms}$ state from a ten-step context. Training uses 978 KSTAR discharges from 2017--2022, with 101 held out for testing. The 457-million-parameter model attains $R^2=0.987$ for normalized pressure and $0.956$ for $H_{89}$, with spectrogram PSNRs of 30.1 and $23.0\,\mathrm{dB}$. Predicted spectra reproduce ELM and tearing-mode signatures together with their associated performance changes. Feeding the predictions to OASIS yields 97.3% L/H classification accuracy, exceeding a dedicated 94.5% baseline without Thomson scattering or $D_\alpha$ input. Results are limited to one device, so multi-machine transfer remains unverified.

### Contributions

1. Formulated tokamak prediction as joint generative modeling of scalar performance, controls, and magnetic-fluctuation spectrograms.
2. Developed a VQ-VAE plus causal-Transformer architecture for self-supervised next-state prediction of multimodal plasma signals.
3. Showed that widely available Mirnov-coil and standard control signals can replace costly spatial diagnostics for the evaluated tasks.
4. Improved normalized-pressure prediction and downstream L/H classification on held-out KSTAR shots.
5. Demonstrated physically coherent forecasts of ELMs and tearing modes and quantified the benefit of increasing model size.
