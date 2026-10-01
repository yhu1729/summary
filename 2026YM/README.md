# 2026YM

## ChatGPT (July 2026)

### Summary

This paper analyzes an explicit Adams-Bashforth-type integrator (ABTI) built from complex-time sampling and a Cauchy-integral discretization. Although numerical evidence had suggested that its absolute-stability regions approach a nonzero limiting semicircle as the order grows, harmonic-analysis arguments disprove that conjecture: the parabolic stability radius ultimately tends to zero, albeit much more slowly than for classical Adams-Bashforth formulas. The authors derive a characteristic polynomial for the amplification matrix and a computable condition relating a prescribed parabolic radius to the largest admissible approximation order. They also show that the original reconstruction loses one order of accuracy and give a correction that restores the intended order. For parabolic partial differential equations, tensor-product spectral analysis yields a sharp CFL restriction, $L^2$ stability, and error estimates. Numerical tests on ordinary and parabolic differential equations confirm the predicted orders and show instability when the time step crosses the derived CFL boundary.

### Contributions

1. Disproved the conjectured nonzero limiting stability region for arbitrary-order ABTI schemes.
2. Derived a characteristic polynomial and an order-versus-parabolic-radius stability criterion.
3. Identified the source of the original method's one-order accuracy loss and supplied a correction.
4. Established CFL-based $L^2$ stability and error bounds for parabolic PDE discretizations.
5. Verified the corrected convergence orders and sharp stability threshold numerically.
