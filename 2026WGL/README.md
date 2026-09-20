# 2026WGL

## ChatGPT (July 2026)

### Summary

Using a validated EAST passive-conductor representation and the Tokamak Simulation Code, the study constructs diverted equilibria and extracts vertical growth rates from free-drift trajectories of the plasma center. Parameter scans show that outward radial displacement improves passive stabilization; increasing minor radius strongly lowers growth by simultaneously reducing elongation and moving the plasma nearer the passive conductor; elongation itself increases growth approximately linearly. Growth rises with plasma current, with a much steeper slope above roughly 800 kA, and increases with internal inductance as the current profile becomes more peaked. A database of 160 equilibria supports a compact backpropagation neural network mapping seven global parameters to growth rate. Training on 120 cases gives mean absolute error 8.11, while 40 test cases give 10.45; randomized-input tests indicate acceptable robustness through about 3% relative error. The model is intended for predesign stability screening, not replacement of detailed equilibrium calculations.

### Contributions

1. Built a TSC free-drift workflow using an experimentally and TokSys-validated EAST passive-structure model.
2. Established how radial position and minor radius alter passive vertical stabilization.
3. Found approximately linear elongation dependence and a steeper current dependence above about 800 kA.
4. Showed that more peaked current profiles, represented by higher internal inductance, increase growth rate.
5. Trained a seven-input neural network on 160 equilibria and quantified its prediction error and input robustness.
