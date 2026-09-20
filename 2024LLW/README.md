# 2024LLW

## ChatGPT (July 2026)

### Summary

This paper develops deterministic and uncertainty-quantification solvers for the Vlasov--Poisson system with massless electrons near the quasineutral limit. Because the nonlinear Poisson equation contains $e^\phi$, classical particle-in-cell discretizations inherit restrictive Debye-length and plasma-frequency scales. The authors differentiate and reformulate that field equation, then construct an explicit asymptotic-preserving particle-in-cell method whose spatial and temporal resolution need not track the small Debye length. Numerical tests show stable long-time behavior and convergence toward the quasineutral model as $\varepsilon\to0$ on a fixed mesh. For random initial data, the high-fidelity kinetic solver is paired with an Euler--Poisson low-fidelity model in a stochastic-collocation bi-fidelity procedure. Low-fidelity snapshots select a reduced basis, while a small number of high-fidelity runs supplies its coefficients. Tests with five-dimensional random inputs and a Karhunen--Loève expansion report roughly $10^{-3}$ errors with as few as five high-fidelity runs in one case, with accurate means and standard deviations across $\varepsilon=0.01$ to $1$.

### Contributions

1. Reformulated the nonlinear Vlasov--Poisson field equation to remain suitable in the quasineutral limit.
2. Constructed an explicit asymptotic-preserving particle-in-cell discretization for massless electrons.
3. Demonstrated fixed-mesh convergence to the quasineutral system over short and long simulations.
4. Coupled the kinetic solver to an Euler--Poisson surrogate through a reduced bi-fidelity stochastic-collocation method.
5. Validated efficient uncertainty estimates for multiple random-data models and plasma regimes.
