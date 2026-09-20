# 2026S4

## ChatGPT (July 2026)

### Summary

The state-dependent Riccati equation (SDRE) method approximates nonlinear optimal feedback control by expressing nonlinear dynamics in a state-dependent linear form and repeatedly solving algebraic Riccati equations. This paper relates the resulting quadratic value-function approximation to the Hamilton--Jacobi--Bellman equation. It derives a computable residual from Lyapunov equations for derivatives of the Riccati solution and bounds the value-function error by residual integrals along optimal and SDRE-controlled trajectories; an explicit local bound follows under exponential stability. Because semilinear representations are nonunique, the paper characterizes residual-minimizing representations and proves the existence of a zero-residual choice when two admissible representations produce opposite residual signs. Computationally, it compares a first-order offline--online approximation with a cascade Newton--Kleinman method warm-started from the previous time step. Tests on a controlled nonlinear Zeldovich reaction--diffusion equation show that cascade Newton--Kleinman matches direct Riccati solves at much lower cost and remains stable in cases where the offline--online method diverges.

### Contributions

1. Expressed SDRE suboptimality through the Hamilton--Jacobi--Bellman residual of its approximate value function.
2. Derived residual-integral error bounds and a local norm bound under exponential stability.
3. Established conditions for a semilinear representation with vanishing residual and formulated residual minimization otherwise.
4. Gave a computable sufficient condition for stability of the offline--online closed-loop approximation.
5. Showed that cascade Newton--Kleinman is faster than direct Riccati solves and more robust than the offline--online approximation on a nonlinear PDE control problem.
