# 2026RLLW

## ChatGPT (July 2026)

### Summary

This work ports RMC criticality calculations to GPUs through a unified CPU--GPU data-transfer framework and four GPU-oriented techniques. Refined Event Parallelism groups particle work by spatial cell and reaction type to reduce thread divergence. Parallel Atomic Tally distributes scoring across small atomic arrays, while Parallel Atomic Bank stores fission neutrons with near-optimal memory use. A pool-managed hierarchical cache retains geometry levels and cross sections. Tests on a fuel assembly, KRUSTY, VENUS-II, and a full pressurized-water-reactor core agree with CPU RMC within $2$ pcm in $k_{\mathrm{eff}}$; full-core mesh-flux errors remain below $1\%$, averaging about $0.1\%$. At $10^6$ particles per generation, one RTX 4090 delivers performance comparable to roughly 140--150 CPU cores, and Refined Event Parallelism is up to 5.35 times faster than GPU history-based tracking. Benefits diminish for small particle populations and simple geometries because kernel-launch and scheduling costs dominate.

### Contributions

1. Designed an automatic CPU--GPU class-data mapping framework that reduces porting boilerplate by more than 90%.
2. Developed Refined Event Parallelism using spatial-cell and reaction-type hashing to suppress branch divergence.
3. Introduced Parallel Atomic Tally, improving transport efficiency by 20--60% over a single atomic tally.
4. Introduced Parallel Atomic Bank, reaching at least 96% relative storage efficiency at $10^6$ particles.
5. Validated RMC-GPU on four reactor models and quantified its accuracy, scaling, and workload-dependent limits.
