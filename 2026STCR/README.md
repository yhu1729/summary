# 2026STCR

## ChatGPT (July 2026)

### Summary

This paper redesigns PLUTO's Lagrangian Particle module for GPU-enabled gPLUTO simulations of nonthermal particles in relativistic magnetized astrophysical flows. Each computational particle represents an ensemble whose energy spectrum evolves through adiabatic changes, synchrotron and inverse-Compton losses, and first-order Fermi acceleration at shocks. The C++ implementation uses OpenACC for NVIDIA GPU offloading and MPI across nodes, restructures particle data for coalesced access, compacts deleted particles, and overlaps particle exchange with container resizing. Verification recovers the expected second- and third-order particle-advection convergence and matches the analytical post-shock spectral slope within 0.5%. Strong- and weak-scaling tests on MareNostrum 5 and Leonardo cover up to 28,672 CPU cores and 1,024 GPUs. Weak-scaling efficiency remains above 90% on CPUs and approximately 80--90% on GPUs. Comparing complete nodes, four GPUs outperform 112 CPU cores by about $4\times$ for the shock case and $6\times$ for advection. OpenACC currently limits accelerator portability to NVIDIA hardware; an OpenMP port is planned.

### Contributions

1. Re-engineered PLUTO's nonthermal Lagrangian-particle module as GPU-compatible C++ within gPLUTO.
2. Implemented OpenACC/MPI particle storage, compaction, boundary exchange, and spectral-update workflows.
3. Verified particle-advection order and shock-accelerated spectral evolution against analytical solutions.
4. Demonstrated strong and weak scaling through 28,672 CPU cores and 1,024 GPUs on two EuroHPC systems.
5. Measured full-node GPU speedups of roughly $4\times$ for shock evolution and $6\times$ for advection.
