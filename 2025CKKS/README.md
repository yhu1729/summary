# 2025CKKS

## ChatGPT (July 2026)

### Summary

The paper develops asymptotic-preserving conservative semi-Lagrangian discontinuous Galerkin (AP-CSLDG) schemes for the one-dimensional Vlasov--Poisson system as the normalized Debye length $\lambda$ approaches zero. Direct discretization becomes stiff and the Poisson equation degenerates in this quasi-neutral limit. The authors instead combine a conservative semi-Lagrangian Vlasov solver with a reformulated Poisson equation obtained from the kinetic equation's moments. Semi-Lagrangian transport removes the CFL restriction and conserves particle number, while high-order DG approximation resolves fine phase-space structure. The paper proves asymptotic consistency and stability, showing that the schemes remain well behaved without resolving the Debye length in space or time. Landau damping, two-stream instability, and bump-on-tail tests assess accuracy and behavior in both quasi-neutral and non-quasi-neutral regimes; the AP variants retain reliable solutions on under-resolved meshes at per-step costs comparable to explicit schemes. The analysis and experiments are restricted to a one-dimensional electrostatic model with well-prepared initial data; electromagnetic, collisional, multidimensional, and unsplit extensions are left open.

### Contributions

1. Combined conservative semi-Lagrangian DG transport with a moment-based reformulated Poisson equation.
2. Proved asymptotic consistency and stability as the Debye length tends to zero.
3. Removed both CFL and Debye-length resolution restrictions while exactly conserving total particle number.
4. Constructed splitting variants with per-step costs comparable to explicit Vlasov--Poisson solvers.
5. Validated the schemes on Landau damping, two-stream, and bump-on-tail problems across quasi-neutral regimes.
