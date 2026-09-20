# 2025YHR

## ChatGPT (July 2026)

### Summary

Particle-in-cell methods efficiently follow collisionless plasma characteristics, but common Monte Carlo collision operators add noise and usually provide only first-order temporal accuracy. This paper develops a deterministic particle treatment of the nonlinear Lenard--Bernstein--Dougherty Fokker--Planck operator and couples it to Vlasov field dynamics. Kernel regularization turns the collision term into a particle velocity field, while a local optimization enforces discrete conservation of mass, momentum, and kinetic energy. A fully explicit second-order integrator then applies an accuracy-preserving velocity correction so that particle plus field energy is conserved at the fully discrete level. The construction covers electrostatic Ampere and electromagnetic Maxwell formulations and provides a more robust correction variant for rare particles whose nominal factor is not real. Cell lists remove negligible distant interactions, and GPU evaluation accelerates the otherwise quadratic collision calculation. Homogeneous relaxation tests recover near second-order velocity accuracy and Maxwellian relaxation. Collisional linear and nonlinear Landau damping and two-stream benchmarks preserve energy substantially better than forward-Euler or Verlet comparisons while reproducing expected collisional smoothing. Remaining work includes a convergence proof and broader electromagnetic validation.

### Contributions

1. Constructed a deterministic particle discretization of the nonlinear Fokker--Planck collision operator.
2. Enforced discrete mass, momentum, and kinetic-energy conservation through a local optimization procedure.
3. Developed a fully explicit second-order correction that conserves total particle--field energy exactly at the discrete level.
4. Extended the energy-conserving construction to both electrostatic and electromagnetic plasma systems.
5. Demonstrated accuracy and robustness on relaxation, Landau-damping, and two-stream benchmarks with cell-list and GPU acceleration.
