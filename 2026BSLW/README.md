# 2026BSLW

## ChatGPT (July 2026)

### Summary

This paper co-designs an MPI extension and HPE Slingshot 11 implementation that removes the CPU from the fast path of two-sided GPU communication while retaining familiar MPI semantics. Persistent requests separate setup from repeated communication; `MPI_Match` permanently resolves partners before execution, and an `MPI_Queue` orders matched request starts and waits with GPU-stream kernels. The prototype maps these abstractions to libfabric deferred work queues, triggered operations, and GPU-accessible counters while preserving receiver-buffer readiness. A Cabana `StreamHalo` implementation shows that gather and scatter exchanges can enqueue receives, packing, sends, completion waits, and unpacking without host synchronization. On Frontier and Tuolumne, stream-triggered ping-pong lowers latency by as much as 50% for small and medium messages, although the untuned prototype loses to production MPI for large messages and some small non-ready sends. A CabanaGhost strong-scaling benchmark reaches 8,192 Frontier GPUs and improves maximum mean speedup by 28% for the large problem. Source code, run scripts, raw measurements, and analysis are released.

### Contributions

1. Designed a CPU-free GPU communication API around MPI persistent operations, permanent matching, and stream-associated queues.
2. Preserved two-sided matching and remote-buffer-readiness semantics outside the GPU--NIC critical path.
3. Implemented the API on Slingshot 11 using libfabric deferred work queues, triggered operations, and counters.
4. Integrated the abstraction into Cabana halo exchanges with only limited changes to conventional MPI structure.
5. Demonstrated up to 50% lower ping-pong latency and 28% higher maximum strong-scaling speedup on leadership-class systems.
