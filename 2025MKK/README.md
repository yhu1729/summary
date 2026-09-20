# 2025MKK

## ChatGPT (July 2026)

### Summary

This paper proposes theoretical foundations for GPU-native compilation as a way to reduce latency in AI-assisted code iteration. The premise is that current code generation, compilation, execution, and testing workflows pay large CPU--GPU transfer costs. The authors outline three approaches: adapting traditional compilation passes for parallel GPU execution, using neural sequence-to-sequence compilation with probabilistic verification, and combining the two in hybrid systems. They derive latency and energy bounds that suggest traditional GPU compilation could improve iteration by transfer elimination, while neural compilation could gain more from massive parallelism. The paper also formalizes a probabilistic verification framework in which compilation accuracy can be traded against parallel exploration. The analysis is speculative and systems-oriented rather than an implementation report, but it gives a structured model for evaluating future compilers designed around GPU-resident AI coding loops.

### Contributions

1. Identified CPU--GPU transfer latency as a bottleneck in AI code-iteration workflows.
2. Classified traditional, neural, and hybrid approaches to GPU-native compilation.
3. Derived theoretical latency and energy bounds for the proposed approaches.
4. Formalized probabilistic verification for neural compilation candidates.
5. Connected GPU-native compilation to self-improving AI systems and rapid testing loops.
