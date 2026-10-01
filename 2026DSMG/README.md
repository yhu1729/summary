# 2026DSMG

## ChatGPT (July 2026)

### Summary

Selective state-space models avoid attention's quadratic sequence cost, but their recurrent state updates, local convolutions, and packed mixer parameters make conventional Transformer tensor parallelism inefficient. This paper develops a state-space-model-specific multi-GPU inference design. It caches each layer's recurrent state after prefill so decode does not reprocess the prompt, shards channels so convolution and state updates remain local, and explicitly distributes packed quantities such as $\Delta$, $B$, $C$, $A$, and $D$ according to their computational roles. Communication is restricted mainly to output aggregation, where optional FP32-to-FP16 all-reduce reduces bandwidth. Experiments cover Mamba, Mamba-2, Falcon-Mamba, and Zamba on NVIDIA A6000 PCIe and A100 NVLink systems. Tensor parallelism supports prompts two to four times longer at fixed batch size and substantially improves throughput over single-GPU inference, particularly for long contexts. Quantized communication provides further gains but slightly changes token rankings, making it an explicit accuracy--throughput trade-off.

### Contributions

1. Introduced a distributed, sharded state-space-model cache that carries recurrent state from prefill into decode without extra communication.
2. Designed channel-wise tensor partitioning that keeps convolution, gating, and recurrent state updates GPU-local.
3. Separated packed mixer fields and placed channel-dependent, token-dependent, and replicated parameters according to their data dependencies.
4. Added optional FP32-to-FP16 quantized all-reduce at the remaining synchronization boundary.
5. Evaluated the design across four pure and hybrid state-space architectures on PCIe- and NVLink-connected GPU systems.
