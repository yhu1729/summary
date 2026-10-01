# 2026CLY

## ChatGPT (July 2026)

### Summary

This paper constructs a semi-Lagrangian scalar auxiliary variable (SAV) method for the Vlasov-Ampere and Vlasov-Maxwell equations. Standard Eulerian or semi-Lagrangian splittings often preserve either Gauss's law or total energy, but not both, because the Ampere and transport pieces are separated. The authors introduce an auxiliary scalar variable that reformulates the energy while retaining a splitting compatible with semi-Lagrangian transport. The resulting method preserves Gauss's law without solving the constraint equation and preserves a modified total energy, while keeping an explicit update structure. The paper develops the method first for Vlasov-Ampere, then for 1d-2v and full Vlasov-Maxwell systems, and tests it on standard plasma benchmarks. Numerical comparisons show stable behavior and improved invariant preservation relative to methods that enforce only one structure. Remaining work includes non-Fourier spatial discretizations for complex geometries, Maxwell-step CFL improvements, and possible PIC adaptations.

### Contributions

1. Introduced an SAV reformulation for Hamiltonian Vlasov-Ampere and Vlasov-Maxwell dynamics.
2. Designed a splitting that preserves Gauss's law while supporting semi-Lagrangian transport.
3. Preserved a reformulated total energy without requiring a costly implicit nonlinear solve.
4. Extended the construction from Vlasov-Ampere to 1d-2v and full Vlasov-Maxwell models.
5. Demonstrated the method on numerical tests against invariant-preserving alternatives.
