# 2026TKCD

## ChatGPT (July 2026)

### Summary

This paper directly programs NVIDIA FP64 tensor cores to accelerate small, irregular matrix products in matrix-free high-order finite-element kernels. Tensor contractions in MFEM are decomposed into small dense products and mapped to DMMA PTX instructions for Grace Hopper GH200 and Grace Blackwell GB200 GPUs; custom layouts handle unsupported shapes, and kernel fusion further reduces data motion. The tensor-core kernels cut shared-memory reads by $4.6\times$, improve individual kernel throughput by up to 59%, and raise energy efficiency by up to 27%. Combined with fusion, they deliver up to $2\times$ speedup and up to 83% energy savings. In a production tsunami digital-twin application, all kernel variants show near-ideal weak scaling, while the optimized code reaches 90% strong-scaling efficiency across 9,216 GH200 GPUs on Alps. The optimizations are under review for inclusion in the public MFEM repository.

### Contributions

1. Designed direct FP64 tensor-core mappings for the small, irregular matrix products in high-order finite-element operators.
2. Identified shared-memory traffic as the main bottleneck and reduced reads by $4.6\times$.
3. Combined DMMA kernels with operator fusion to obtain up to $2\times$ speedup and 83% energy savings.
4. Compared GH200 and GB200 performance and energy behavior for small FP64 tensor-core operations.
5. Demonstrated near-ideal weak scaling and 90% strong-scaling efficiency on up to 9,216 GPUs in a production tsunami application.
