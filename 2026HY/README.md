# 2026HY

## ChatGPT (July 2026)

### Summary

Vlasov--Poisson solutions in the quasi-neutral regime oscillate on the small plasma period, making standard explicit and implicit schemes expensive or inaccurate. This paper introduces analytically solvable asymptotic-preserving (ASAP) splitting schemes by reformulating Vlasov--Poisson as a constrained Vlasov--moment--Ampère system. Moment equations reduce the nonlinear field subproblem to an analytically solvable ordinary differential equation, and characteristics then give the distribution function; both split subproblems therefore have no temporal discretization error. The schemes preserve the plasma frequency, temporal waveforms, and quasi-neutral limit. At the time-discrete level they also conserve global mass and energy, preserve a maximum principle and Casimir invariants, and retain time-reversal symmetry for Vlasov--Ampère equations. Experiments up to $3D3V$ reproduce highly oscillatory dynamics with steps substantially larger than the plasma period and outperform classical Hamiltonian splitting. Rigorous error bounds showing dependence on the Debye length remain future work.

### Contributions

1. Reformulated Vlasov--Poisson into constrained subproblems that admit analytical time evolution.
2. Constructed splitting schemes that preserve plasma frequency, waveform, and the quasi-neutral asymptotic limit.
3. Established discrete conservation of mass and energy together with maximum-principle and Casimir preservation.
4. Extended the construction to Vlasov--Ampère equations while retaining time-reversal symmetry.
5. Demonstrated accurate large-step simulations, including a six-dimensional phase-space problem.
