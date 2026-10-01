# 2025HL

## ChatGPT (July 2026)

### Summary

The paper generalizes alternating Anderson acceleration into a periodic scheme, $\mathrm{aAA}(m)[s]\text{--}\mathrm{FP}[t]$, that performs $t$ fixed-point steps followed by $s$ Anderson steps with window size $m$. For linear Richardson iteration, it relates the full-history, single-Anderson-step variant to GMRES, proves convergence when the fixed-point map is contractive, and gives a sufficient condition for diagonalizable noncontractive iteration matrices. Experiments cover ill-conditioned nonsymmetric linear systems, Navier--Stokes Picard solves, regularized logistic-regression gradient descent, and ADMM for nonlinear nonsmooth optimization. Suitable $m,s,t$ choices reduce iterations and runtime relative to unaccelerated iterations, windowed Anderson acceleration, and the earlier $s=1$ scheme; ADMM and gradient-descent cases show roughly order-of-magnitude acceleration. Performance remains parameter-dependent, and large Anderson windows can make the internal least-squares problem rank deficient.

### Contributions

1. Defined the flexible periodic $\mathrm{aAA}(m)[s]\text{--}\mathrm{FP}[t]$ family.
2. Established a periodic connection between full-history alternating Anderson acceleration and GMRES.
3. Proved convergence for contractive linear fixed-point maps.
4. Gave a sufficient convergence condition for diagonalizable noncontractive Richardson matrices.
5. Demonstrated acceleration across linear solvers, Navier--Stokes, gradient descent, and ADMM while identifying limitations.
