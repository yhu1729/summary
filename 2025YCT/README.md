# 2025YCT

## ChatGPT (July 2026)

### Summary

CARMA is a server-scale resource manager that collocates multiple deep-learning training tasks on a GPU while controlling out-of-memory failures and performance interference. It combines per-second GPU telemetry, warm-up-aware bookkeeping that waits for a task's first kernel, risk filters over compute and memory activity, and placement policies based on available memory or utilization. Optional Horus, PyTorch FakeTensor, and GPUMemNet estimators predict task memory demand; an OOM recovery queue relaunches failed tasks on an idle GPU. Experiments on two production-trace-derived workloads running on four NVIDIA A100 GPUs show that the best recovery-based policy reduces makespan by about $35\%$. Reported aggregate gains include $54\%$ higher streaming-multiprocessor activity, $61\%$ higher occupancy, $62\%$ higher memory use, and roughly $15\%$ lower GPU energy. Memory estimators reduce or eliminate OOMs but can overpredict demand and suppress useful collocation. CARMA targets one server and exposes a throughput-versus-per-task-latency trade-off; cluster-scale scheduling, fairness, and interference-aware task matching remain future work.

### Contributions

1. Designed a task-level collocation manager integrating GPU monitoring, risk analysis, placement, memory estimation, and OOM recovery.
2. Introduced time-to-first-kernel bookkeeping that prevents premature collocation while a newly launched task is still warming up.
3. Evaluated memory- and utilization-aware policies with three distinct GPU-memory estimators and recovery-only baselines.
4. Implemented lightweight recovery that detects an OOM-failed task and relaunches it on a fully idle GPU.
5. Demonstrated approximately $35\%$ lower makespan and $15\%$ lower GPU energy for the best policy on a trace-derived training workload.
