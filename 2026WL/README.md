# 2026WL

## ChatGPT (July 2026)

### Summary

High-resolution ordinary differential equations use backward error analysis to expose behavior hidden by continuous limits of optimization algorithms. Existing $O(s^r)$-resolution theory assumes the update map satisfies $g(z,0)=z$, excluding many momentum methods. This paper introduces an $O((\sqrt{s})^r)$-resolution framework that allows momentum, lifted states, and variable parameters, covering heavy-ball, Nesterov acceleration, and accelerated mirror methods. It proves local and finite-time global approximation bounds and derives correction terms systematically. At low resolution, heavy-ball and Nesterov methods share the same ODE; at $O(\sqrt{s})$, Nesterov contains Hessian-driven damping while heavy-ball contains only a velocity correction, explaining their different stability. The authors then design high-resolution corrections for primal--dual hybrid gradient and heavy-ball methods. Lyapunov analysis proves globally optimal convergence rates for the corrected schemes. Numerical tests show that corrected PDHG removes limit cycles on bilinear saddle problems and that corrected heavy-ball converges more stably and rapidly on a standard piecewise-quadratic counterexample.

### Contributions

1. Extended high-resolution backward-error ODE analysis to momentum methods that violate $g(z,0)=z$.
2. Established systematic $O((\sqrt{s})^r)$-resolution models with local and finite-horizon approximation bounds.
3. Distinguished Nesterov and heavy-ball dynamics through Hessian-driven damping versus velocity correction.
4. Derived corrected primal--dual hybrid gradient and heavy-ball algorithms from their high-resolution ODEs.
5. Proved optimal convergence rates and validated the predicted stability improvements numerically.
