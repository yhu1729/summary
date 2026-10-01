# 2026BKSS

## ChatGPT (July 2026)

### Summary

The paper constructs a strongly history-independent, fully dynamic two-choice balls-and-bins allocation. Its representation depends only on the current ball set and fixed randomness, so snapshots reveal no update history. For at most $m$ balls on $n$ bins, the final algorithm guarantees maximum load $m/n+O(1)$ with high probability while requiring only $O(\log\log(m/n))$ expected ball movements per insertion or deletion. The construction begins with a canonically ordered history-independent greedy baseline, then develops Slice and Spread, which repeatedly removes excess balls above carefully chosen thresholds and reallocates them using fresh second-choice randomness. A history-independent cuckoo-hashing-style cleanup converts small cumulative overload into constant maximum overload. The result improves even the prior unrestricted fully dynamic trade-off by combining constant overload with $o(m/n)$ expected recourse.

### Contributions

1. Formalized strongly history-independent dynamic two-choice allocation through unique representability from the current set and random tape.
2. Analyzed canonical-order history-independent greedy, including its recourse behavior over a broad parameter range.
3. Introduced Slice and Spread, whose thresholded rounds progressively smooth loads while retaining low update sensitivity.
4. Developed a history-independent cuckoo-hashing cleanup that turns low cumulative overload into $O(1)$ maximum overload.
5. Proved maximum load $m/n+O(1)$ with high probability and $O(\log\log(m/n))$ expected recourse per operation.
