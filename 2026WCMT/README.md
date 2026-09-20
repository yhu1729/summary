# 2026WCMT

## ChatGPT (July 2026)

### Summary

Exascale particle-in-cell Monte Carlo plasma simulations can generate data faster than file-based workflows can store and analyze it. This work modernizes the electrostatic BIT1 code with OpenMP task parallelism in the particle mover and an openPMD data layer backed by ADIOS2. Besides conventional BP4 files, the Sustainable Staging Transport engine streams checkpoints directly from simulation processes to analysis and visualization consumers in memory. Time-dependent checkpointing lets downstream tools inspect evolving particle and field data without stopping the simulation or routing every step through persistent storage. Profiling with gprof, perf, IPM, and Darshan separates computational, communication, and I/O costs and compares the legacy path with BP4 and SST configurations. The resulting hybrid MPI+OpenMP workflow improves runtime, data availability, and interactive analysis while reducing pressure on the storage system. The paper demonstrates an integrated route to in-situ plasma diagnostics rather than treating simulation, output, and visualization as separate stages.

### Contributions

1. Added OpenMP task-based parallelism to the BIT1 particle mover.
2. Integrated openPMD as a portable interface for particle and field checkpoints.
3. Enabled in-memory ADIOS2 SST streaming from simulation to analysis consumers.
4. Supported time-dependent in-situ visualization without interrupting the running calculation.
5. Profiled and compared legacy file I/O, ADIOS2 BP4, and SST workflows.
