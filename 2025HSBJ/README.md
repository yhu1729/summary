# 2025HSBJ

## ChatGPT (July 2026)

### Summary

This paper reverse-engineers NVIDIA Collective Communication Library (NCCL) 2.19.1 to explain how GPU collectives are executed across devices and nodes. It traces communicator setup, channel partitioning, CUDA block and warp roles, buffer slots, and intra- and inter-node transports, including GPUDirect P2P, shared memory, sockets, InfiniBand verbs, and GPUDirect RDMA. The analysis contrasts Simple, LL, and LL128 protocols: Simple favors large transfers, LL minimizes small-message latency, and LL128 combines flag-based synchronization with 120-byte payloads but requires suitable atomic-write semantics. Ring and tree collectives are decomposed into NCCL communication primitives and classified by whether loop iterations can pipeline. Benchmarks on 16 Grace Hopper nodes show that LL/LL128 and trees favor small messages, while Simple and rings dominate large inter-node transfers; LL128 remains strong within a node over NVLink. These implementation findings underpin ATLAHS, whose NCCL-aware schedules model large-scale training communication with reported simulation errors below 5%.

### Contributions

1. Documented NCCL's channel, buffer, CUDA-thread, and protocol execution hierarchy from its implementation.
2. Explained the synchronization, payload, bandwidth, and hardware trade-offs of Simple, LL, and LL128.
3. Mapped intra- and inter-node paths through P2P, shared-memory, socket, InfiniBand, and GPUDirect RDMA transports.
4. Decomposed ring and tree collectives into communication primitives and pipelined or non-pipelined iteration patterns.
5. Connected the analysis to ATLAHS and validated protocol and algorithm regimes on a 16-node GH200 system.
