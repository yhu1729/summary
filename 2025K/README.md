# 2025K

## ChatGPT (September 2026)

### Summary

Kwon gives a way to turn online regret-minimizing algorithms into iterations for finding fixed points of nonexpansive maps. The central inequality bounds squared fixed-point residuals by terms that online algorithms control through regret, so a regret guarantee becomes a residual guarantee. Converting online gradient descent recovers Krasnoselskii--Mann iteration, including a projected form for maps whose outputs need not lie in the feasible set. Converting AdaGrad-Norm yields best-iterate residual bounds adaptive to an unknown scalar scaling of the map; diagonal and full-matrix AdaGrad variants adapt to unknown preconditioners. The matrix guarantees require bounded iterates for convergence, and the adaptive bounds generally concern the best iterate rather than the last. Illustrative experiments on Markov-chain stationary distributions, total-variation image denoising, and zero-sum games compare the methods with problem-specific baselines and show faster or more robust convergence in some settings. The comparisons concern selected instances and iteration counts, not runtime or broad benchmark averages.

### Contributions

1. Converted regret bounds into fixed-point residual bounds using the equivalence between nonexpansive maps and cocoercive residual operators.
2. Recovered Krasnoselskii--Mann iteration from online gradient descent and derived projected iterations for non-self maps.
3. Proved AdaGrad-Norm best-iterate bounds that adapt to an unknown favorable scalar scaling.
4. Extended the analysis to diagonal and full-matrix AdaGrad updates that adapt to unknown positive-definite preconditioners.
5. Tested the resulting iterations on Markov chains, image denoising, and zero-sum games, documenting both gains and limitations against the chosen baselines.
