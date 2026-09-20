# 2025TFSF

## ChatGPT (July 2026)

### Summary

Using 1,251 JET ITER-like-wall H-mode pedestals from the EUROfusion database, this study reconstructs electron-temperature profiles from density profiles and engineering parameters. Global neural networks predict unseen profiles within about 20% of experiment, while local models establish that the task is learnable from local quantities augmented by radial position. Separatrix loss power, plasma current, fuelling rate, and strike-point configuration are the most informative engineering inputs. Physics-motivated reconstructions find $\eta_e=L_{n_e}/L_{T_e}\approx2$ in the steep-gradient region but a broad overall distribution, inconsistent with a single marginal slab-electron-temperature-gradient threshold. A flexible scaling $R/L_{T_e}=A(R/L_{n_e})^\alpha$ gives a database-wide $\alpha\approx0.4$; pulse-specific fits place $A$ and $\alpha$ on a common similarity line. Gyrokinetics-inspired heat-flux models improve on database-wide marginal models, particularly when the heat flux scales quadratically with $R/L_{T_e}$, but retain systematic shape errors and often require an unphysical negative critical $\eta_e$. This gap from machine-learning accuracy exposes missing pedestal-transport physics and limits device generalization.

### Contributions

1. Demonstrated accurate data-driven temperature-pedestal reconstruction across a large JET-ILW dataset.
2. Ranked the engineering parameters that most improve global and local predictions.
3. Quantified the broad pedestal distribution of $\eta_e$ and its steep-gradient mean near two.
4. Discovered a pulse-spanning similarity relation between power-law gradient-model parameters.
5. Diagnosed specific successes and physical shortcomings of gyrokinetics-inspired heat-flux closures.
