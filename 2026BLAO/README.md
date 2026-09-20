# 2026BLAO

## ChatGPT (July 2026)

### Summary

TokaMind is an open-source multi-modal transformer pretrained on public MAST tokamak diagnostics spanning time series, two-dimensional profiles, and videos with different sampling rates and missing signals. Fixed-basis DCT3D embeddings, masked attention and losses, a shared transformer, modality heads, and per-target adapters permit partial parameter reuse across changing input and output schemas. Pretraining uses 16 diagnostics, five actuators, and 34 targets; the Base and Tiny models contain $6.93$ million and $3.69$ million parameters. On the 14-task TokaMark benchmark, fine-tuned Base achieves overall normalized root-mean-square error $0.212$, compared with $0.249$ for the strongest benchmark baseline and $0.229$ for matched-epoch training from scratch. It wins 13 of 14 tasks and 52 of 57 signal outputs; pretraining helps most for long-horizon and high-dimensional equilibrium tasks. Evaluation is confined to MAST, does not establish cross-device transfer, and leaves rapidly varying and long-horizon signals challenging.

### Contributions

1. Introduced an open-source foundation model for heterogeneous tokamak diagnostics.
2. Provided schema-flexible masking, tokenization, and adapters for missing or changing signals.
3. Used lightweight DCT3D embeddings that outperform the tested learned codecs.
4. Improved overall TokaMark error to $0.212$ and won 13 of 14 tasks.
5. Showed that pretraining transfers most clearly to long-horizon and high-dimensional objectives.
