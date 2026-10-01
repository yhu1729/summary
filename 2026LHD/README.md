# 2026LHD

## ChatGPT (September 2026)

### Summary

This paper presents jaxdae, a JAX-native solver for differential-algebraic equations (DAEs), which combine differential evolution with constraints that must hold at each time. It combines adaptive BDF, Radau, and Rosenbrock integration with Pantelides index reduction, dummy derivatives, and acausal assembly of coupled physical components. The adaptive BDF gradient uses a custom reverse rule: it records the accepted time grid, freezes that grid, and re-solves a variable-step BDF-2 problem for its adjoint. This avoids differentiating discontinuous step-acceptance decisions; the gradient is the adjoint of the replay problem, not exactly of the forward adaptive solve. BDF and fixed-step Rosenbrock paths support JAX differentiation, whereas Radau is forward-only. Order tests, cross-solver comparisons, gradient checks, and chemical, nuclear, and power-system examples evaluate the implementation. On measured GPU benchmarks, compiled batched gradients remain nearly flat in wall time through batch size 1,000 for small models; comparison runs for the PyTorch counterpart reach only batch size 10. The work leaves distributed multi-GPU execution and wider event-adjoint verification open.

### Contributions

1. Integrated implicit DAE solvers, structural index reduction, and acausal multiphysics assembly in JAX.
2. Implemented a frozen-grid BDF-2 replay adjoint for adaptive solves that composes with `jax.grad`, `vmap`, and `jit`.
3. Verified fixed-step BDF orders one through five and checked DAE gradients against finite differences and independent references.
4. Demonstrated batched GPU gradient throughput and parameter-inference workflows in chemical and nuclear models.
5. Documented the replay-adjoint approximation and the present limits of Radau differentiation, event handling, and multi-GPU execution.
