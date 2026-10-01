# 2002S

## ChatGPT (August 2026)

### Summary

This review recasts adaptive time-stepping for ordinary differential and differential-algebraic equations as a feedback-control problem. After logarithmic transformation, the relation between step size and estimated local error becomes an approximately linear discrete process, making control-theoretic stability analysis applicable. Elementary controllers can generate irregular steps or poor tolerance response; proportional--integral controllers instead yield smoother step sequences, predictable tolerance proportionality, and robust work--precision behavior. Predictive controllers extend this approach to implicit and stiff integration by estimating changes in the principal error function. The paper also coordinates step-size selection with modified Newton iterations: measured convergence rates determine when to reuse a Jacobian, refactor a matrix, or reject and retry a step. This replaces disconnected heuristics with interacting controllers whose dynamics can be analyzed. Computational stability and tolerance proportionality are proposed as software-quality criteria alongside accuracy and efficiency. The framework is broadly applicable, but its detailed recommendations depend on reliable local-error and iteration-convergence estimates; multistep controller dynamics and differential-algebraic error estimation remain incompletely understood.

### Contributions

1. Formulated adaptive time-stepping as a discrete feedback-control problem through logarithmic models of step size and local error.
2. Analyzed elementary controllers and advocated proportional--integral designs that stabilize step sequences and improve tolerance proportionality.
3. Developed predictive controllers for implicit and stiff solvers by estimating changes in the principal error function.
4. Coordinated time-step control with modified Newton convergence monitoring, Jacobian reevaluation, and matrix refactorization.
5. Introduced computational stability and tolerance proportionality as practical measures of adaptive solver quality and identified unresolved controller problems.
