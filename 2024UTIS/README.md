# 2024UTIS

## ChatGPT (July 2026)

### Summary

This survey organizes GPU-centric communication: mechanisms that reduce CPU participation in the critical path of multi-GPU data movement and synchronization. It introduces separate intra-node and inter-node taxonomies based on where APIs execute and whether data traverse device, host, or network paths, distinguishing host-native, host-controlled, device-native, and fallback modes. The paper traces vendor mechanisms across NVIDIA, AMD, and Intel, including peer access, unified or virtual memory, GPUDirect RDMA, and GPU-initiated networking. It then compares higher-level ecosystems such as GPU-aware MPI, NCCL/RCCL/oneCCL, NVSHMEM/ROC_SHMEM/Intel SHMEM, UCX, and related research libraries, emphasizing that API placement alone does not determine the data path. Research directions include CPU-free networking, topology-aware collective scheduling, communication-computation overlap, debugging and profiling for multi-GPU races, fault tolerance, and compression-accelerated communication. The survey also identifies practical gaps: vendor fragmentation, inconsistent terminology, limited cross-vendor portability, and insufficient tools for fine-grained device-native transfers and multi-GPU race detection.

### Contributions

1. Defined GPU-centric communication in terms of reduced CPU involvement rather than a single API or transport technology.
2. Developed operation-based taxonomies for intra-node and inter-node communication control and data paths.
3. Mapped NVIDIA, AMD, and Intel hardware, runtime, memory-management, and networking mechanisms into a common framework.
4. Compared major collective, one-sided, MPI, and middleware libraries across capabilities, limitations, and reported performance behavior.
5. Synthesized open problems in CPU-free networking, topology awareness, overlap, debugging, resilience, portability, and compressed communication.
