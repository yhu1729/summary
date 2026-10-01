# 2025LMST

## ChatGPT (July 2026)

### Summary

A tree shortcutting adds distance-preserving edges to reduce the number of hops between vertices. Classical constant-hop constructions are globally sparse but contain dense subgraphs. This paper initiates a systematic study of shortcuttings constrained by arboricity and treewidth, two measures of how tree-like a graph remains. It proves upper and lower bounds on the hop-diameter--treewidth tradeoff, including optimal bounds through hop diameter $O(\log\log n)$ and lower bounds for every larger value. Together these imply $\text{hop-diameter}\times\text{treewidth}=\Omega((\log\log n)^2)$ for all hop diameters, resolving a prior open question even for paths. The constructions also yield constant-hop $(1+\varepsilon)$-spanners of doubling metrics with arboricity $O(\log^* n)$. A three-hop fixed-port routing scheme with $O(\log^2 n/\log\log n)$ local bits resolves another open problem. The results connect structural sparsity of tree shortcuttings to geometric spanners and compact routing.

### Contributions

1. Formulated tree shortcutting under explicit tree-likeness constraints measured by treewidth and arboricity.
2. Established optimal hop-diameter--treewidth tradeoffs up to $O(\log\log n)$ hops.
3. Proved all-regime lower bounds, including the product bound $\Omega((\log\log n)^2)$ even for paths.
4. Built constant-hop $(1+\varepsilon)$-spanners for doubling metrics with arboricity $O(\log^* n)$.
5. Derived a three-hop compact routing scheme with $O(\log^2 n/\log\log n)$ local memory.
