# 2026WBBC

## ChatGPT (July 2026)

### Summary

This tutorial organizes inversion-based shape control (IBSC), the common tokamak-control strategy that linearizes an equilibrium to map actuator currents or voltages to shape changes and then inverts that map. It unifies static current-response and dynamic voltage-response formulations, pseudoinverse and quadratic-program inversions, actuator and shape weighting, regularization, filtering, and saturation constraints. The authors emphasize failure modes caused by singular directions, poor units or scaling, actuator limits, model mismatch, and interactions between shape and vertical-position loops. They provide a systematic design and validation workflow, supported by extensive appendices, and apply it to NSTX-U. The original controller allowed shape commands to interfere with rapid vertical stabilization, producing a vertical-position ``bobble.'' A decoupling construction removes this interaction in simulation while retaining upper- and lower-null control. The actuator study also shows that adding PF1A and PF2 to the vertical-control set improves simulated phase margin by $6^\circ$. The results are control-design predictions based on linearized models and simulations; commissioning performance will still depend on model fidelity, nonlinear limits, diagnostics, and the actual power-supply dynamics.

### Contributions

1. Unified major static, dynamic, unconstrained, and constrained variants of IBSC in one framework.
2. Catalogued conditioning, scaling, saturation, modeling, and loop-interaction failure modes.
3. Supplied a systematic controller-design procedure and implementation-oriented tutorials.
4. Diagnosed NSTX-U's vertical bobble as coupling between shape and vertical-control commands.
5. Removed the simulated bobble through decoupling and identified PF1A/PF2 as phase-margin-improving actuators.
