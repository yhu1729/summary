# 2026OPK

## ChatGPT (July 2026)

### Summary

The paper formalizes quadratization for spatially one-dimensional autonomous partial differential equations (PDEs): introducing auxiliary variables so every evolution equation becomes at most quadratic in the original variables, their spatial derivatives, and the auxiliaries. It proves that every polynomial PDE of spatial differential order $h$, under sufficient regularity, admits a monomial quadratization of differential order $3h$, while finding a minimum-order monomial quadratization is NP-hard. The authors then introduce QuPDE, a symbolic algorithm for polynomial or rational PDE formulas. It enumerates monomial decompositions, verifies candidate lifts, searches with branch and bound, and polynomializes rational expressions. Pruning and ordering heuristics make the combinatorial search practical. Tests on fourteen PDE models from fluid mechanics, space physics, chemical engineering, and biology produce low-order lifts in every case. Several lifts use fewer auxiliaries than earlier transformations, while other examples are quadratized computationally for the first time. The work concerns symbolic reformulation rather than well-posedness or numerical solution of the lifted boundary-value problems.

### Contributions

1. Gave a rigorous definition of PDE quadratization, including quadratization order and differential order.
2. Proved existence of a monomial quadratization of differential order $3h$ for polynomial PDEs of order $h$.
3. Proved that optimal monomial PDE quadratization is NP-hard by reduction from the ordinary-differential-equation problem.
4. Developed QuPDE by combining symbolic decomposition, candidate verification, branch-and-bound search, and rational polynomialization.
5. Demonstrated low-order quadratizations on fourteen PDE benchmarks, including improved and previously unknown lifts.
