# 2025A

## ChatGPT (July 2026)

### Summary

This paper presents a machine-checked proof of a C routine that converts a coordinate-form sparse matrix into compressed sparse row form. The algorithm sorts coordinate triples by row and column, combines duplicate entries, and fills the CSR value, column-index, and row-pointer arrays from left to right. Its implementation is short, but correctness depends on detailed relationships among partially consumed COO entries, partially constructed CSR arrays, duplicate sums, row boundaries, allocation sizes, and machine-integer bounds. The author develops the invariants bottom-up from the obligations of the Verified Software Toolchain's separation-logic proof, while using Coq definitions to specify when COO and CSR matrices represent the same mathematical matrix. The specification and supporting lemmas required 1,571 lines of Coq, followed by 412 lines of VST proof. Formalization uncovered five implementation bugs: four off-by-one errors and one unsigned-integer initialization defect. The resulting verified module is intended as a composable component for larger verified numerical programs, including finite-element software that constructs sparse matrices.

### Contributions

1. Produced a machine-checked functional-correctness proof for a C COO-to-CSR conversion routine.
2. Specified duplicate aggregation and mathematical equivalence between COO and CSR representations.
3. Demonstrated a bottom-up method for deriving intricate loop invariants from proof obligations.
4. Found and corrected five concrete implementation defects during formal verification.
5. Delivered a verified sparse-matrix construction component suitable for composition in larger numerical programs.
