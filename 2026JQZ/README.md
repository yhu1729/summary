# 2026JQZ

## ChatGPT (July 2026)

### Summary

This paper develops explicit extended integrating factor Runge-Kutta schemes of fourth through sixth order for the Allen-Cahn equation that preserve its maximum bound principle without a time-step restriction. The framework relaxes earlier constraints on exponential coefficients and constructs a target-order method recursively from a method one order lower. Rather than solving increasingly complicated Runge-Kutta order conditions directly, it interprets the local truncation requirement through Duhamel's formula and uses Gauss quadrature to determine suitable stages and coefficients. The authors prove maximum-bound preservation and $L^\infty$-error estimates for the resulting eIFRK4-6 schemes. Two- and three-dimensional tests confirm their formal temporal orders, bound preservation, and favorable energy behavior. In long-time phase-field simulations with large steps, eIFRK6 remains substantially more accurate and stable than lower-order stabilized IFRK schemes, although unconditional discrete energy dissipation is not established.

### Contributions

1. Introduced a relaxed extended-IFRK framework for high-order explicit schemes with unconditional maximum-bound preservation.
2. Gave a recursive construction in which a lower-order method supplies nonlinear values at quadrature nodes for the target-order method.
3. Connected Runge-Kutta order requirements to Duhamel-formula local error and used Gauss quadrature to derive eIFRK4-6 formulas.
4. Proved unconditional maximum-bound preservation and optimal temporal $L^\infty$-error estimates for orders four through six.
5. Demonstrated formal convergence, bound preservation, and robust long-time behavior in two- and three-dimensional phase-field tests.
