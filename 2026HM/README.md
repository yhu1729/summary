# 2026HM

## ChatGPT (July 2026)

### Summary

This preprint develops a priori adaptive algorithms for estimating finite blow-up times of autonomous ordinary differential equations. Rather than following an unbounded solution indefinitely, each method selects a tolerance-dependent radius whose hitting time approximates the true blow-up time, then applies forward Euler steps scaled by the sensitivity of that auxiliary hitting time. Separate algorithms cover scalar and multidimensional systems under stated growth, regularity, and monotonicity assumptions. Both attain $O(\epsilon)$ blow-up-time error at $O(\epsilon^{-1})$ computational cost. For representative scalar problems, the analysis shows that uniform first-order stepping incurs at least an additional logarithmic cost factor. Numerical tests include polynomial, exponential, and logarithmically modified growth laws, uncoupled and coupled systems, and a semidiscretized reaction--diffusion equation. Experiments recover the predicted rates and illustrate extensions to higher-order integrators and some problems outside the main assumptions.

### Contributions

1. Recast blow-up-time estimation as a tolerance-controlled auxiliary hitting-time problem.
2. Designed sensitivity-weighted adaptive algorithms for scalar and multidimensional autonomous ODEs.
3. Proved $O(\epsilon)$ error with $O(\epsilon^{-1})$ work for both algorithms.
4. Quantified the asymptotic efficiency gain over uniform first-order time stepping.
5. Validated the theory across diverse ODEs and a semidiscretized reaction--diffusion model.
