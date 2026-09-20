# 2026KJWC

## ChatGPT (July 2026)

### Summary

PCGBandit accelerates transient PDE simulations without pretrained models or additional simulations by learning from linear solves generated during the run itself. Each preconditioner choice is treated as an arm in a nonstationary adversarial-bandit problem, with solve wall time as feedback. A reduced-variance Tsallis-INF variant adaptively selects among 33 incomplete-Cholesky, thresholded incomplete-Cholesky, and multigrid configurations; its learning update costs $O(d)$, independent of matrix size. A fallback to IC(0) preserves solver convergence when a selected configuration reaches its iteration limit. Integrated into OpenFOAM, the method is evaluated on six fluid, multiphase, and magnetohydrodynamic simulations. It is optimal or near-optimal across the tested tasks, exceeds both static baselines by more than fourfold for some linear-solve workloads, and usually breaks even within roughly $10^3$ solves, often within $10^2$. Deterministic operation-count feedback remains within 1.2 times the wall-clock-feedback result, improving reproducibility. The simplest direct-numerical-simulation case receives no net benefit.

### Contributions

1. Cast within-simulation preconditioner selection as an adversarial-bandit problem requiring no training runs.
2. Developed reduced-variance PCGBandit with $O(d)$ learning cost and worst-case $O(\sqrt{dT})$ regret.
3. Added adaptive selection across 33 OpenFOAM preconditioner configurations.
4. Preserved convergence through an IC(0) backstop and deterministic cost feedback.
5. Measured wall-clock and break-even behavior on six fluid and MHD simulations.
