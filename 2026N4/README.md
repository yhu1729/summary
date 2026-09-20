# 2026N4

## Codex/ChatGPT (September 2026)

### Summary

A rank-$23$ scheme multiplies general $3\times3$ matrices using $52$ additions or subtractions in a transformed basis. Its two input linear maps require $12$ additions each and its output map $28$; conversion into and out of this basis is additional work. For recursive multiplication, the paper proves that these conversions cost $O(n^2\log n)$, leaving the leading $O(n^{\log_3 23})$ arithmetic term unchanged. The construction searches an existing database of more than $17{,}000$ multiplication schemes over $\mathbb{F}_2$, using randomized invertible basis changes and a greedy heuristic that reuses intermediate sums. Updating only the affected part of the heuristic's potential reduces each candidate-potential evaluation from $O(mn^2)$ to $O(mn)$. A larger search finds $405$ binary schemes with at most $55$ additions. One $52$-addition computation is lifted to signed arithmetic over general fields by solving sign constraints while preserving its computation graph. Explicit formulas and a symbolic verification script support reproducibility. The result reduces an arithmetic operation count; it does not establish optimality or measured matrix-multiplication throughput.

### Contributions

1. Gives explicit rank-$23$ multiplication formulas with a $52$-addition transformed-basis core, split into $12+12+28$ additions.
2. Proves that recursive input and output basis conversions require only $O(n^2\log n)$ additional arithmetic operations.
3. Reduces candidate-potential evaluation from $O(mn^2)$ to $O(mn)$ by updating only affected column-pair contributions.
4. Combines randomized basis changes with an existing rank-$23$ database to find $405$ binary schemes requiring at most $55$ additions.
5. Lifts a $52$-addition binary computation to signed general-field arithmetic and supplies explicit basis matrices, search instructions, and symbolic verification code.
