# 2025HBMG

## ChatGPT (July 2026)

### Summary

NCCL's GPU-Initiated Networking (GIN) extends device-side communication from intra-node memory access to inter-node RDMA, allowing CUDA kernels to initiate fine-grained transfers without host orchestration. The design has three layers: host APIs create device communicators and register collective memory windows; device APIs expose remote memory operations; and network plugins provide transport-specific execution. A GPUDirect Async Kernel-Initiated backend uses DOCA GPUNetIO for direct GPU-to-NIC commands, while a proxy backend uses lock-free GPU-to-CPU queues to support conventional RDMA hardware with equivalent semantics. GIN shares the NCCL Device API with load/store-accessible and multimemory modes, preserving access to NCCL's topology, collective algorithms, and deployment infrastructure. Integration with the DeepEP mixture-of-experts communication library demonstrates practical device-driven dispatch and combine operations. Benchmarks characterize latency and show where direct initiation reduces software overhead, while the proxy path trades some latency for portability.

### Contributions

1. Added inter-node GPU-initiated RDMA to NCCL's device-side communication model.
2. Defined host setup, device operations, and transport plugins as a three-layer architecture.
3. Implemented direct GPU-to-NIC execution through DOCA GPUNetIO.
4. Supplied compatible proxy semantics for standard RDMA networks through lock-free queues.
5. Demonstrated GIN in DeepEP for fine-grained mixture-of-experts communication.
