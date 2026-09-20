# 2026ABBB

## ChatGPT (July 2026)

### Summary

This workshop report turns cross-disciplinary discussions between numerical linear algebra and theoretical computer science into precise research problems in matrix computation. For linear systems, it proposes parameterized PDE-derived benchmarks and asks for sharper correctness and finite-precision theories for multigrid, conjugate-gradient, sketch-and-project, GMRES, and preconditioning. Its eigenvalue section seeks deterministic substitutes for random pseudospectral shattering, near-optimal precision bounds for diagonalization, and better understanding of Ritz values and invariant subspaces. The low-rank section studies when greedy or randomized column selection and rank-revealing factorizations achieve the strong performance observed in practice, especially for structured matrices. The sketching section separates the weaker notion of subspace injection from embedding, asks whether injections suffice for more numerical tasks, and records near-sharp conjectures for sparse and rerandomized Hadamard maps. The final section extends the agenda to tensor-network approximation, eigenvector-dependent nonlinear eigenproblems from local Hamiltonians, and matrix-sign approximants constrained by multiplication count. Rather than claiming solutions, the report contributes a technically motivated, jointly negotiated agenda with concrete complexity, conditioning, approximation, and precision targets.

### Contributions

1. Formulated a linear-solver agenda around scalable PDE benchmarks and unresolved correctness and convergence questions for multigrid and Krylov methods.
2. Specified eigenvalue challenges involving deterministic pseudospectral shattering, optimal-precision diagonalization, and Ritz and invariant-subspace guarantees.
3. Framed structural conditions under which column subset selection and rank-revealing factorizations should be provably quasi-optimal.
4. Developed open questions for subspace injections, optimal sparse sketches, and rerandomized Hadamard transforms.
5. Extended the program to tensor approximation, nonlinear Hamiltonian eigenproblems, and multiplication-budget-optimal matrix-sign polynomials.
