# 2026BSSK

## ChatGPT (July 2026)

### Summary

This paper ports the energy-conserving semi-implicit particle-in-cell code ECsim to GPUs with OpenACC directives while preserving its MPI decomposition and production code structure. The particle mover and moment-gathering kernels are offloaded after restructuring loops, managing device-resident data, and addressing atomics and particle-to-cell access patterns. Numerical comparisons confirm agreement with the CPU implementation. On Leonardo Booster nodes, the accelerated version achieves about a fivefold reduction in time to solution and a threefold reduction in energy use relative to the CPU baseline. Cross-generation tests show that ECsim's memory-bound kernels benefit from newer bandwidth and that the GH200 unified-memory design reduces data-movement penalties; newer atomic hardware particularly improves moment gathering. Strong scaling retains roughly $70\%$ efficiency through 64 GPUs, and weak scaling retains about $78\%$ through 1,024 GPUs. Comparisons are deliberately limited to the original ECsim implementation because other PIC codes use different algorithms and accuracy-cost tradeoffs.

### Contributions

1. Ported ECsim's dominant particle kernels to GPUs with minimally invasive OpenACC directives.
2. Preserved the code's semi-implicit, machine-precision energy-conserving formulation.
3. Validated GPU results against the original CPU implementation.
4. Quantified time-to-solution and energy-to-solution gains across NVIDIA GPU generations.
5. Demonstrated strong and weak scaling to 64 and 1,024 GPUs, respectively.
