# 2025RW

## ChatGPT (July 2026)

### Summary

This MFCS 2025 paper develops lazy B-trees, an external-memory analogue of lazy search trees. Lazy search trees are sorted dictionaries whose cost adapts automatically to the actual mixture of updates and queries, interpolating between priority-queue-like and binary-search-tree-like behavior. The paper transfers this idea to the block-transfer model so that the I/O savings of B-trees over binary search trees extend to the same adaptive regime. A central obstacle is that lazy search trees depend on biased search trees, while a fully satisfactory external-memory biased-search-tree replacement is not available. The authors construct an external variant with the subset of guarantees needed for lazy B-trees, which is also of independent data-structural interest. The resulting structure supports external-memory sorted dictionaries with lazy updates and includes an external-memory priority-queue special case competitive with specialized heaps, with faster decrease-key and insert operations than known alternatives. The work links adaptive indexing, deferred data structures, and external-memory dictionaries.

### Contributions

1. Introduced lazy B-trees as external-memory lazy search trees for adaptive sorted dictionaries.
2. Generalized B-tree I/O speedups to workloads that interpolate between priority queues and search trees.
3. Built an external-memory biased-search-tree substitute with guarantees sufficient for the lazy-search-tree framework.
4. Derived an external-memory priority-queue special case competitive with specialized heap structures.
5. Connected lazy updates, external memory, database cracking, and deferred data structures in a unified design.
