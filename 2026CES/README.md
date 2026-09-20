# 2026CES

## ChatGPT (July 2026)

### Summary

This paper describes Bandicoot, a C++ GPU linear-algebra library whose Armadillo-compatible interface is intended to ease migration from CPU code. Expression templates encode a user's operation as a compile-time abstract syntax tree. Template specializations traverse that tree to fill reusable skeleton kernels with generated argument lists, indexing expressions, bounds checks, and element operations, thereby fusing compound expressions into one GPU kernel without a runtime expression optimizer or JIT source generator. The implementation separates the high-level API and optimizer from CUDA and OpenCL backends; further backends remain incomplete. Benchmarks on an NVIDIA RTX 4090 compare 32-bit, mostly $10{,}000\times10{,}000$ expressions with several array and machine-learning toolkits after warm-up. Bandicoot is fastest or tied in most reported cases and sustains approximately the measured memory-bandwidth ceiling while adding 2--16 matrices, whereas competitors degrade for longer expressions. These experiments exclude warm-up and cover one GPU, precision, and workload suite, so they establish competitive kernel execution rather than universal application performance.

### Contributions

1. Presented an Armadillo-compatible C++ interface for GPU linear algebra with CUDA and OpenCL backends.
2. Represented compound expressions as compile-time types and generated fused GPU kernel source from their syntax trees.
3. Reused backend-independent skeleton kernels to reduce specialized-kernel implementation and maintenance.
4. Eliminated runtime expression analysis and JIT source-generation infrastructure while retaining device-time kernel compilation.
5. Benchmarked compound expressions and demonstrated sustained measured memory bandwidth for sums of up to sixteen matrices.
