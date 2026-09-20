# 2026RECB

## ChatGPT (July 2026)

### Summary

Physics-based plasma-control models must meet deterministic cycle deadlines, which general-purpose threading runtimes do not target. The authors develop a real-time-safe C11 multithreading library for the DIII-D plasma control system. Worker threads are initialized before a shot, run on isolated cores, and synchronize through acquire--release atomics and spin waiting, avoiding kernel-mediated synchronization during real-time execution. The library parallelizes two production physics codes. Real-time TORBEAM traces independent electron-cyclotron beams for four gyrotrons consistently within a roughly $20$ ms cycle. Real-time STRIDE partitions state-transition-matrix integrations around rational surfaces and computes ideal-stability quantities in about $100$ ms on 72 cores. STRIDE's remaining bottleneck is serial equilibrium-coordinate preprocessing, which consumes most of the runtime. The work demonstrates deployable deterministic parallelism on DIII-D, while the reported timing depends on isolated-core hardware and does not establish portability to every control environment.

### Contributions

1. Designed a C11 multithreading library around deterministic real-time plasma-control constraints.
2. Used precreated workers and acquire--release atomics to avoid nondeterministic kernel synchronization during shots.
3. Deployed real-time TORBEAM for parallel gyrotron ray tracing with approximately $20$ ms execution cycles.
4. Parallelized STRIDE's stability calculation to execute in approximately $100$ ms on DIII-D hardware.
5. Identified serial coordinate preprocessing as the dominant remaining STRIDE performance bottleneck.
