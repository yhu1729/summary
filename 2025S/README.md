# 2025S

## ChatGPT (July 2026)

### Summary

Worst-case sorting complexity depends only on input size and therefore misses structure in partially sorted inputs. The paper proposes a broader view of universal optimality in which an oblivious algorithm, without knowing a problem-dependent parameter in advance, matches the best asymptotic complexity available when that parameter is known. For sorting, it defines maximal $\alpha$-sorted subsequences: input-order subsequences whose elements are contiguous in the final sorted order. A stable partition sort that checks whether each recursive subproblem is already sorted exploits maximal subsequences of sizes $n_1,\ldots,n_k$ without explicitly discovering them. It uses $O\!\left(\sum_i n_i\log(n/n_i+1)\right)$ comparisons, equivalently an entropy-sensitive bound plus $O(n)$. A counting argument gives a matching comparison lower bound for the same family of permutations. The result generalizes multisorting and shows how ordinary partition sorting can adapt to a new presortedness measure, although in-place implementation, practical constants, and other parameterizations remain open.

### Contributions

1. Formulated a parameter-sensitive notion of universal optimality for algorithms with implicit input structure.
2. Defined maximal $\alpha$-sorted subsequences as a new measure of presortedness.
3. Modified stable partition sort to exploit that measure without first computing the subsequences.
4. Proved an entropy-sensitive upper bound based on the maximal-subsequence sizes.
5. Established a matching comparison lower bound and related the result to multisorting and adaptive sorting.
