# 2026OAGT

## ChatGPT (September 2026)

### Summary

Quasi-stationary distributions describe the long-lived behavior of stochastic processes conditioned on avoiding absorption. This paper extends two numerical approaches for computing them. Its deterministic iteration solves the nonlinear quasi-stationary equation for general Markov processes with discrete or continuous state spaces and one or more absorbing states. Its Monte Carlo alternative follows a single trajectory and, after absorption, resets it using states sampled from that trajectory's history. Tests span branching, immigration-death, random-walk, Ornstein--Uhlenbeck, circular-diffusion, SIRS, and SIS models, including cases with analytical solutions. The iterative method is usually more accurate in less time, resolves extremely small probabilities, and estimates rare-event extinction times, while the history-reset Monte Carlo method can retain bias and convergence sensitivity. Monte Carlo is nevertheless easier and sometimes preferable for multidimensional domains with complicated boundaries. Parameter studies show that mild overrelaxation and a concentrated initial distribution accelerate iteration, while spatial and temporal discretization choices impose different accuracy-cost tradeoffs in continuous problems. The comparison therefore provides both generalized algorithms and practical criteria for selecting and tuning them.

### Contributions

1. Generalized nonlinear fixed-point iteration to continuous or discrete Markov processes with multiple absorbing states.
2. Introduced a single-trajectory Monte Carlo reset mechanism based on the trajectory's empirical history.
3. Benchmarked both methods across one- and two-dimensional models with natural and artificial absorbing boundaries.
4. Demonstrated the iterative method's advantage for high accuracy and rare-event probabilities while identifying Monte Carlo bias and convergence failures.
5. Quantified how relaxation, initialization, grid spacing, timestep, system size, and boundary complexity affect efficiency and method choice.
