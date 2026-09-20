# 2026KS

## ChatGPT (July 2026)

### Summary

Universal constructions usually serialize operations through consensus whenever they might conflict in any state, even when they commute in the state actually reached. The paper formalizes dynamic concurrency: an implementation uses a strong synchronization primitive only when an operation can conflict with concurrent operations in a possible object state during its execution. Its construction records operations in a shared acyclic dependency graph and tracks active operations with snapshots. An operation that commutes with every relevant subset of active operations can be committed directly; otherwise, a consensus-based conflict-resolution path orders it. A commit-adopt-like mechanism prevents operations committed through the two paths from bypassing one another. The authors prove linearizability, wait-freedom, and dynamic concurrency for arbitrary sequential objects. This is a possibility result rather than a performance result: conflict-free operations take two write-read rounds, but checking commutativity may require exponential local work in the number of concurrent operations, so avoiding consensus may cost more than it saves.

### Contributions

1. Defined dynamic concurrency for arbitrary sequential objects using state-dependent operation commutativity.
2. Designed a universal construction that uses strong synchronization only when a dynamic conflict is detected.
3. Represented operation dependencies with an acyclic graph whose topological orders are equivalent linearizations.
4. Coordinated direct and consensus-based commits so conflicting operations cannot bypass one another.
5. Proved linearizability, wait-freedom, and dynamic concurrency while identifying the cost of exhaustive conflict detection.
